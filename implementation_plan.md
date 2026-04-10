# Portfolio Web App Implementation Plan

This document outlines the plan for creating a web portfolio to showcase the House Prices Prediction project (Group 11).

## Goal Description

The goal is to build an interactive, visually stunning portfolio website to highlight the data insights, dashboard visualizations, and machine learning model results derived from the Jupyter Notebook (`Nhom11_DAAN436277_23_2_01.ipynb`) and the project report.

## Proposed Architecture

We will build a responsive and highly aesthetic static website using:
- **HTML5**: For semantic page structure.
- **Vanilla CSS (No Tailwind)**: To have fine-grained control over the aesthetic, implementing a vibrant dark theme, glassmorphism effects, flexbox/grid layouts, and smooth micro-animations.
- **Vanilla JavaScript**: For logic, interactivity, and rendering charts.
- **Chart.js (via CDN)**: For plotting interactive and beautiful data visualizations (dashboards) based on the project's data insights.

## Proposed Changes

### Web Application Outline

We will create a new directory `PortfolioWeb/` containing the site inside the workspace.

---

#### [NEW] `PortfolioWeb/index.html`
The main structure of the single-page portfolio, divided into sections:
1. **Hero Section**: Eye-catching title, animated intro, and project overview.
2. **Data Overview**: Summary of the dataset (1460 train samples, 80 features).
3. **Insights Dashboard**: Interactive charts (e.g., Feature Correlation with SalePrice, Target Distribution) using Chart.js.
4. **Model Performance**: A comparison card layout showing the Root Mean Squared Logarithmic Error (RMSLE) for Lasso, ElasticNet, KRR, Gradient Boosting, XGBoost, LightGBM, and the final Stacking Ensemble.
5. **Final Results**: The optimal ensemble weights and final prediction score metrics (RMSLE, R², MAE).

#### [NEW] `PortfolioWeb/styles.css`
The main stylesheet ensuring a **wow-factor** design:
- Premium dark mode color palette (deep blacks, slate grays, vibrant primary accents like neon purple and electric blue).
- Modern typography imported from Google Fonts (e.g., 'Inter' or 'Outfit').
- Glassmorphism effects (translucency + backdrop blur) for data cards.
- CSS transitions and keyframe animations for a dynamic, "alive" feel.

#### [NEW] `PortfolioWeb/script.js`
The logic controlling the interactivity and data rendering:
- Configuration and data initialization for Chart.js (injecting data observed from the notebook, e.g., model scores and sample EDA distributions).
- Smooth scrolling logic for navigation.
- Intersection Observers to trigger fade-in animations as the user scrolls down.

## Open Questions

> [!IMPORTANT]  
> 1. Do you want to include any specific images or charts directly from the `Report.pdf`, or should I use clean `Chart.js` charts to display the metrics based on the data in the notebook? (I recommend Chart.js for interactivity).  
> 2. Do you have a preference for the color scheme (e.g., Dark mode with Blue/Purple accents, or Light mode with minimal colorful aesthetics)?  

## Verification Plan

### Automated Tests
Not applicable for this static web site generation, but I will launch a local server and verify the structure.

### Manual Verification
1. Open `PortfolioWeb/index.html` in a web browser.
2. Verify all sections (Hero, Dashboard, Models, Results) are rendering correctly.
3. Check the responsiveness of the site on smaller viewport dimensions.
4. Ensure the Chart.js graphs load correctly and display the relevant housing data statistics and RMSLE scores.
5. Provide a walkthrough to the user with screenshots/animations.

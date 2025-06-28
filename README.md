# Visual_dashboard
A simple Interactive Data App dashboard made using Streamlit, Pandas, and Plotly

# Setup
Install the required packages:
pip install streamlit pandas plotly

# Step 1: Streamlit + Pandas Dashboard
Let's start by building a functional dashboard using just Streamlit and Pandas. This demonstrates how Streamlit creates interactive web interfaces and how Pandas handles data filtering.

Create a file called dashboard.py:
NWU Data Science
Data skills for decision making.

How to Combine Streamlit, Pandas, and Plotly for Interactive Data Apps
With just two Python files and a handful of methods, you can build a complete dashboard that rivals expensive business intelligence tools.
By Vinod Chugani on June 27, 2025 in Data Science
FacebookTwitterLinkedInRedditEmailShare

How to Combine Streamlit, Pandas, and Plotly for Interactive Data Apps
Image by Author | ChatGPT
 

Introduction
 
Creating interactive web-based data dashboards in Python is easier than ever when you combine the strengths of Streamlit, Pandas, and Plotly. These three libraries work seamlessly together to transform static datasets into responsive, visually engaging applications — all without needing a background in web development.

NWU Data Science
Data skills for decision making.

However, there's an important architectural difference to understand before we begin. Unlike libraries such as matplotlib or seaborn that work directly in Jupyter notebooks, Streamlit creates standalone web applications that must be run from the command line. You'll write your code in a text-based IDE like VS Code, save it as a .py file, and run it using streamlit run filename.py. This shift from the notebook environment to script-based development opens up new possibilities for sharing and deploying your data applications.

Airia Enterprise AI
Schedule a demo today

In this hands-on tutorial, you'll learn how to build a complete sales dashboard in two clear steps. We'll start with core functionality using just Streamlit and Pandas, then enhance the dashboard with interactive visualizations using Plotly.

 

Setup
 
Install the required packages:

pip install streamlit pandas plotly
 

Create a new folder for your project and open it in VS Code (or your preferred text editor).

 

Step 1: Streamlit + Pandas Dashboard
 
Let's start by building a functional dashboard using just Streamlit and Pandas. This demonstrates how Streamlit creates interactive web interfaces and how Pandas handles data filtering.

Create a file called step1_dashboard_basic.py:

# key Streamlit methods used here:

st.set_page_config() configures the browser tab title and layout
st.sidebar creates the left navigation panel for filters
st.multiselect() generates dropdown menus for user selections
st.columns() creates side-by-side layout sections
st.metric() displays large numbers with labels
st.dataframe() renders interactive data tables
These methods automatically handle user interactions and trigger app updates when selections change.

# Run this from your terminal (or VS Code's integrated terminal):
streamlit run dashboard.py

Your browser will open to http://localhost:8501 showing an interactive dashboard.

# Step 2: Add Plotly for Interactive Visualizations
Now let's enhance our dashboard by adding Plotly's interactive charts. This shows how all three libraries work together seamlessly. Let's create a new file and call it dashboard_plotly.py:

#Run this from your terminal (or VS Code's integrated terminal):
streamlit run dashboard_plotly.py

The Plotly charts are fully interactive — you can hover over data points, zoom in on specific time periods, and even click legend items to show/hide data series.

# How the Three Libraries Work Together
This combination is powerful because each library handles what it does best:

# Pandas manages all data operations:
Creating and loading datasets
Filtering data based on user selections
Aggregating data for visualizations
Handling data transformations

# Streamlit provides the web interface:
Creates interactive widgets (multiselect, sliders, etc.)
Automatically reruns the entire app when users interact with widgets
Handles the reactive programming model
Manages layout with columns and containers

# Plotly creates rich, interactive visualizations:
Charts that users can hover, zoom, and explore
Professional-looking graphs with minimal code
Automatic integration with Streamlit's reactivity

# Next Steps
Try these enhancements:
Add real data:

# Replace sample data with CSV upload
uploaded_file = st.sidebar.file_uploader("Upload CSV", type="csv")
if uploaded_file:
    df = pd.read_csv(uploaded_file)
 

Keep in mind that real datasets will require preprocessing steps specific to your data structure. You'll need to adjust column names, handle missing values, and modify the filter options to match your actual data fields. The sample code provides a template, but each dataset will have unique requirements for cleaning and preparation.

More chart types:

# Pie chart for product distribution
fig_pie = px.pie(filtered_df, values='Sales', names='Product', title='Sales by Product')
st.plotly_chart(fig_pie)

# Deploymet Link: https://visualdashboard-zpd6ctrngonkqgrds4ysgd.streamlit.app/
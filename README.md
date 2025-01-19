# Visualizing Data Using Amazon QuickSight  

In this AWS project, I visualized data using **Amazon QuickSight**, **Amazon S3**, and **Bright Data**. I obtained a dataset from **Bright Data**, stored it in an S3 bucket, and connected it to **Amazon QuickSight** to analyze and visualize patterns based on brand, categories, price, and more.  

---

## Project Overview  

This project involved using **Amazon QuickSight** to create interactive visualizations from a dataset sourced from **Bright Data**. Instead of manually handling the data, I leveraged an **S3 bucket** and a **manifest.json** file to integrate the dataset into QuickSight seamlessly.  

---

## AWS Services Used  

- **Amazon S3** – Stored the dataset and the manifest file.  
- **Amazon QuickSight** – Used for data visualization and insights.  
- **Bright Data** – Provided the dataset for analysis.  

---

## Implementation Steps  

### 1. Obtaining the Dataset  

I sourced the dataset from **Bright Data** in **CSV format**. Since QuickSight requires structured access, I created a **manifest.json** file to specify the dataset’s location in **Amazon S3**.  

### 2. Creating an S3 Bucket  

To store my dataset, I created an **S3 bucket**:  

- Logged into the **AWS Management Console**.  
- Navigated to **S3** and created a new bucket named:  quicksight-bucket-22


- Configured the bucket settings and ensured it had the necessary permissions.  

### 3. Uploading the Dataset  

After setting up the bucket, I uploaded the **CSV dataset**:  

- Opened the **S3 bucket**.  
- Clicked **Upload** and selected the dataset file.  
- Waited for the upload process to complete.  

### 4. Editing and Uploading the Manifest File  

To link QuickSight with my dataset, I edited the **manifest.json** file to include my bucket details:  

```json
{
"fileLocations": [
  {
    "URIPrefixes": [
      "s3://quicksight-bucket-22/dataset.csv"
    ]
  }
],
"globalUploadSettings": {
  "format": "CSV",
  "delimiter": ",",
  "textQualifier": "\"",
  "containsHeader": "true"
}
}

```

### Uploading the Manifest File  

I then uploaded this `manifest.json` file into the **same S3 bucket** as the dataset.  

---

## 5. Connecting Amazon QuickSight  

Once my dataset was in place, I configured **Amazon QuickSight** to access it:  

- Opened **Amazon QuickSight** and signed up.  
- Navigated to **Datasets** and clicked **"New Dataset"** → Selected **S3**.  
- Pasted the **S3 URL** of the `manifest.json` file in the provided space.  
- Named the dataset and clicked **Connect**.  

---

## 6. Creating Data Visualizations  

With the dataset successfully connected, I explored different visualizations such as:  

✅ **Bar Charts** – To compare **brands** and **categories**.  
✅ **Line Graphs** – To identify **pricing trends** over time.  
✅ **Pie Charts** – To display **data distributions**.  

Using **filters, aggregations, and calculated fields**, I extracted **deeper insights** from the dataset.  

---

## Conclusion  

By implementing this setup, I successfully:  

✅ Stored my dataset in **Amazon S3**.  
✅ Connected **Amazon QuickSight** to analyze the dataset.  
✅ Created **interactive visualizations** for meaningful insights.  

This project helped me gain **hands-on experience** with **AWS data services** and **data visualization techniques**. 🚀  


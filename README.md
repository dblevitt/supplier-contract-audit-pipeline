# Supplier Contract Audit Pipeline

This project is a cloud-powered tool for auditing supplier contract data, built in Python using Google Colab and AWS S3. It automatically identifies common data quality issues—such as expired contracts, missing membership levels, duplicate IDs, and pricing anomalies—and generates an exception summary report for review.

---

## Features

- ✅ Pulls contract data from AWS S3 securely
- ✅ Flags expired contracts and missing membership levels
- ✅ Detects duplicate Contract IDs and price outliers
- ✅ Calculates a custom Data Quality Score for each contract
- ✅ Exports exception summary to Excel and uploads it back to S3
- ✅ Includes visualization and sample follow-up email logic

---

## Technologies Used

- Python (Pandas, Matplotlib, XlsxWriter)
- Google Colab (interactive execution and visualization)
- AWS S3 (data input/output)
- Boto3 (AWS SDK for Python)

---

## How It Works

1. **Load Data**: The notebook securely connects to your AWS S3 bucket to retrieve contract data.
2. **Validate Contracts**: It checks for expiration, missing values, duplicates, and unusual pricing.
3. **Score Records**: A Data Quality Score (0–100) flags records that may require manual attention.
4. **Visualize & Report**: Results are charted and saved to a timestamped Excel file.
5. **Upload Back to S3**: The summary is written back to S3 for easy access and team sharing.

---

## Credentials

To run this notebook, you’ll need:
- An AWS IAM user with `s3:GetObject` and `s3:PutObject` permissions
- Access Key ID and Secret Access Key  
(*Tip: Use `getpass.getpass()` in Colab to keep credentials secure*)

---

## Output

The notebook generates:
- An Excel report with separate tabs for each issue type
- A simple bar chart showing issue counts
- A draft supplier email for expired contracts

---

## License

This project is for educational and demonstration purposes.

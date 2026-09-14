# Exam Data Storage

This folder contains all student exam registration data and payment records.

## Folder Structure

```
data/
├── submissions/          # Individual exam applications (JSON format)
├── payments/            # Payment verification records
├── students/            # Student profiles and history
└── reports/             # Generated reports and analytics
```

## File Naming Convention

### Submissions
- Format: `submissions/TSKA-EXM-YYYY-MMDD-{studentId}.json`
- Example: `submissions/TSKA-EXM-2025-0914-001.json`

### Payments
- Format: `payments/PAY-YYYY-MMDD-{utrNumber}.json`
- Example: `payments/PAY-2025-0914-UPI1234567890.json`

### Student Profiles
- Format: `students/{membershipNo}.json`
- Example: `students/TSKA-001.json`

## Data Fields Reference

### Student Information
- fullName (string)
- membershipNo (string)
- dob (date)
- sex (string)
- phone (string)

### Examination Details
- currentBelt (string)
- examBelt (string)
- examFee (number)
- examDate (date)
- examPlace (string)
- attendance (number)
- recommendation (string)
- instructorName (string)
- fatherName (string)

### Payment Information
- utrNumber (string)
- amount (number)
- paymentDate (date)
- paymentStatus (string: pending/verified)
- paymentScreenshot (base64 or file reference)

## Data Privacy

⚠️ **Important**: This repository is public. Avoid storing:
- Full phone numbers
- Complete DOB
- Payment screenshots
- Bank/UPI details

Instead, store encrypted hashes or references.

---

Last Updated: 2025-09-14

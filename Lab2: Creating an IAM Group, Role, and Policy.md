# Overview

This lab guides you through creating an AWS Identity and Access Management (IAM) group, role, and policy in your AWS account. You will perform hands-on tasks to set up these IAM resources and prepare submission details for the IAM Group/Role/Policy AutoGrader. This activity reinforces your understanding of IAM resource relationships and prepares you for secure AWS resource management.

---

### 1. Log in to the AWS Management Console

- Navigate to [https://console.aws.amazon.com](https://console.aws.amazon.com) and sign in to your AWS account (e.g., account ID: `236921907600`).

---

### 2. Access the IAM Service

- In the AWS Console, search for **IAM** and select the **IAM** service.

---

### 3. Create an IAM Policy

- In the IAM dashboard, click **Policies** in the left menu, then click **Create policy**.
- Choose the **JSON** tab and enter a simple policy like:

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": "s3:ListBucket",
      "Resource": "*"
    }
  ]
}
```

- Click **Next**, name the policy (e.g., `AIAcademyPolicy-KCT`), and click **Create policy**.
- **Note the policy ARN**, e.g., `arn:aws:iam::236921907600:policy/StudentPolicy`.

---

### 4. Create an IAM Group

- In the IAM dashboard, click **User groups** in the left menu, then click **Create group**.
- Name the group (e.g., `AIAcademyGroup-KCT`).
- Attach the policy you created by searching for `AIAcademyPolicy-KCT`.
- Click **Create group**.
- **Note the group name**, e.g., `AIAcademyGroup-KCT`.

---

### 5. *(Optional)* Add an IAM User to the Group

- If you created an IAM user (e.g., `aia.kctolentino` from Lab Activity 1), go to **Users**, select the user, and click **Add user to groups**.
- Select `AIAcademyGroup-KCT`, then click **Add to groups**.

---

### 6. Create an IAM Role

- In the IAM dashboard, click **Roles** in the left menu, then click **Create role**.
- Select **AWS service** as the trusted entity and choose **Lambda** (or another service as instructed).
- Attach the policy you created (`AIAcademyPolicy-KCT`).
- Click **Next**, name the role (e.g., `AIAcademyRole-KCT`), and click **Create role**.
- **Note the role name**, e.g., `AIAcademyRole-KCT`.

---

### Key Concepts

- **IAM Group**: A collection of IAM users that share the same permissions, simplifying management.
- **IAM Role**: An entity with permissions that can be assumed by AWS services or users, often used for temporary access.
- **IAM Policy**: A JSON document defining permissions for users, groups, or roles.

## JSON Format
```json
{
   "group_name": "", 
   "role_name": "",
   "policy_arn": "", 
}
```



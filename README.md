# AWS IAM Custom Policies Lab

## 📌 Objective

This lab demonstrates how to create **custom AWS IAM policies** using the **Visual Editor** and review their **JSON representation** while applying the **principle of least privilege**.

Custom policies were created for:

* Amazon EC2
* Amazon S3
* Amazon DynamoDB

---

## 🧠 Skills Demonstrated

* IAM policy design
* Least privilege access control
* Visual Editor usage
* IAM policy JSON analysis
* AWS security best practices

---

## 🛠 Tools & Services Used

* AWS IAM
* Amazon EC2
* Amazon S3
* Amazon DynamoDB

---

## 🏗 Architecture Overview

* IAM policies are created as **customer-managed policies**
* Policies can later be attached to IAM users, groups, or roles
* Permissions are explicitly defined per service

---

## 🔐 What Is an IAM Policy?

An IAM policy is a JSON document that defines:

* Allowed or denied actions
* Target AWS resources
* Conditions for access

IAM follows a **default deny** security model.

---

## 🧪 Lab Tasks

### 1️⃣ EC2 Read-Only Policy

* Service: EC2
* Access level: **Read**
* Resources: All

**Policy name**

```
EC2Policy

{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "VisualEditor0",
            "Effect": "Allow",
            "Action": [
                "ec2:GetIpamResourceCidrs",
                "ec2:GetInstanceUefiData",
                "ec2:GetIpamPoolCidrs",
                "ec2:GetImageBlockPublicAccessState",
                "ec2:GetSnapshotBlockPublicAccessState",
                "ec2:GetEbsEncryptionByDefault",
                "ec2:ExportClientVpnClientConfiguration",
                "ec2:GetHostReservationPurchasePreview",
                "ec2:GetRouteServerPropagations",
                "ec2:GetConsoleScreenshot",
                "ec2:GetLaunchTemplateData",
                "ec2:GetSerialConsoleAccessStatus",
                "ec2:GetEbsDefaultKmsKeyId",
                "ec2:GetRouteServerAssociations",
                "ec2:GetIpamPrefixListResolverRules",
                "ec2:GetIpamPrefixListResolverVersions",
                "ec2:GetIpamDiscoveredResourceCidrs",
                "ec2:GetEnabledIpamPolicy",
                "ec2:GetManagedPrefixListEntries",
                "ec2:ExportVerifiedAccessInstanceClientConfiguration",
                "ec2:GetNetworkInsightsAccessScopeContent",
                "ec2:GetReservedInstancesExchangeQuote",
                "ec2:GetPasswordData",
                "ec2:GetAssociatedIpv6PoolCidrs",
                "ec2:GetSpotPlacementScores",
                "ec2:GetAwsNetworkPerformanceData",
                "ec2:GetImageAncestry",
                "ec2:GetIpamDiscoveredAccounts",
                "ec2:GetResourcePolicy",
                "ec2:GetDefaultCreditSpecification",
                "ec2:StartDeclarativePoliciesReport",
                "ec2:GetCapacityReservationUsage",
                "ec2:GetNetworkInsightsAccessScopeAnalysisFindings",
                "ec2:GetSubnetCidrReservations",
                "ec2:GetConsoleOutput",
                "ec2:ExportClientVpnClientCertificateRevocationList",
                "ec2:GetFlowLogsIntegrationTemplate",
                "ec2:GetSecurityGroupsForVpc",
                "ec2:GetActiveVpnTunnelStatus",
                "ec2:GetIpamDiscoveredPublicAddresses",
                "ec2:GetCoipPoolUsage",
                "ec2:GetAllowedImagesSettings",
                "ec2:GetCapacityManagerMetricData",
                "ec2:GetAssociatedEnclaveCertificateIamRoles",
                "ec2:GetIpamAddressHistory",
                "ec2:GetCapacityManagerAttributes",
                "ec2:GetDeclarativePoliciesReportSummary",
                "ec2:GetCapacityManagerMetricDimensions",
                "ec2:GetManagedPrefixListAssociations",
                "ec2:GetInstanceTpmEkPub",
                "ec2:GetIpamPrefixListResolverVersionEntries",
                "ec2:GetRouteServerRoutingDatabase"
            ],
            "Resource": "*"
        }
    ]
}
```

### 2️⃣ S3 List, Tagging, and Write Policy

* Service: S3
* Access levels:

  * List
  * Tagging
  * Write
* Resources: All

**Policy name**

```
S3Policy
```

### 3️⃣ DynamoDB Full Access Policy

* Service: DynamoDB
* Access level: **All actions**
* Resources: All

**Policy name**

```
DynamoDBPolicy
```

## 📄 Policy JSON

The JSON versions of all policies are stored in the `policies/` directory for review and learning.

---

## ✅ Validation

Lab validation confirmed:

* EC2 policy created successfully
* S3 policy created successfully
* DynamoDB policy created successfully

---

## 📚 Key Takeaways

* IAM policies are the foundation of AWS security
* Explicit allow is required for access
* Least privilege reduces attack surface
* Visual Editor simplifies policy creation
* JSON review is critical for auditing

---

## 🚀 Future Improvements

* Add resource-level restrictions
* Use condition keys (IP, MFA, time-based)
* Attach policies to IAM roles
* Monitor usage with AWS CloudTrail

---

## 👤 Author

**Suriya**
Cybersecurity | Cloud Security Learner

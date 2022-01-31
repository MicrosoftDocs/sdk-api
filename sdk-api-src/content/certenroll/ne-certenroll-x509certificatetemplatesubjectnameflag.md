---
UID: NE:certenroll.X509CertificateTemplateSubjectNameFlag
title: X509CertificateTemplateSubjectNameFlag (certenroll.h)
description: Contains values that specify server and client actions concerning subject names.
helpviewer_keywords: ["SubjectAlternativeNameEnrolleeSupplies","SubjectAlternativeNameRequireDNS","SubjectAlternativeNameRequireDirectoryGUID","SubjectAlternativeNameRequireDomainDNS","SubjectAlternativeNameRequireEmail","SubjectAlternativeNameRequireSPN","SubjectAlternativeNameRequireUPN","SubjectNameAndAlternativeNameOldCertSupplies","SubjectNameEnrolleeSupplies","SubjectNameRequireCommonName","SubjectNameRequireDNS","SubjectNameRequireDirectoryPath","SubjectNameRequireEmail","X509CertificateTemplateSubjectNameFlag","X509CertificateTemplateSubjectNameFlag enumeration [Security]","certenroll/SubjectAlternativeNameEnrolleeSupplies","certenroll/SubjectAlternativeNameRequireDNS","certenroll/SubjectAlternativeNameRequireDirectoryGUID","certenroll/SubjectAlternativeNameRequireDomainDNS","certenroll/SubjectAlternativeNameRequireEmail","certenroll/SubjectAlternativeNameRequireSPN","certenroll/SubjectAlternativeNameRequireUPN","certenroll/SubjectNameAndAlternativeNameOldCertSupplies","certenroll/SubjectNameEnrolleeSupplies","certenroll/SubjectNameRequireCommonName","certenroll/SubjectNameRequireDNS","certenroll/SubjectNameRequireDirectoryPath","certenroll/SubjectNameRequireEmail","certenroll/X509CertificateTemplateSubjectNameFlag","security.x509certificatetemplatesubjectnameflag"]
old-location: security\x509certificatetemplatesubjectnameflag.htm
tech.root: security
ms.assetid: 0880bb94-d26f-49a7-9749-f8be272fa4f6
ms.date: 12/05/2018
ms.keywords: SubjectAlternativeNameEnrolleeSupplies, SubjectAlternativeNameRequireDNS, SubjectAlternativeNameRequireDirectoryGUID, SubjectAlternativeNameRequireDomainDNS, SubjectAlternativeNameRequireEmail, SubjectAlternativeNameRequireSPN, SubjectAlternativeNameRequireUPN, SubjectNameAndAlternativeNameOldCertSupplies, SubjectNameEnrolleeSupplies, SubjectNameRequireCommonName, SubjectNameRequireDNS, SubjectNameRequireDirectoryPath, SubjectNameRequireEmail, X509CertificateTemplateSubjectNameFlag, X509CertificateTemplateSubjectNameFlag enumeration [Security], certenroll/SubjectAlternativeNameEnrolleeSupplies, certenroll/SubjectAlternativeNameRequireDNS, certenroll/SubjectAlternativeNameRequireDirectoryGUID, certenroll/SubjectAlternativeNameRequireDomainDNS, certenroll/SubjectAlternativeNameRequireEmail, certenroll/SubjectAlternativeNameRequireSPN, certenroll/SubjectAlternativeNameRequireUPN, certenroll/SubjectNameAndAlternativeNameOldCertSupplies, certenroll/SubjectNameEnrolleeSupplies, certenroll/SubjectNameRequireCommonName, certenroll/SubjectNameRequireDNS, certenroll/SubjectNameRequireDirectoryPath, certenroll/SubjectNameRequireEmail, certenroll/X509CertificateTemplateSubjectNameFlag, security.x509certificatetemplatesubjectnameflag
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: X509CertificateTemplateSubjectNameFlag
req.redist: 
ms.custom: 19H1
f1_keywords:
 - X509CertificateTemplateSubjectNameFlag
 - certenroll/X509CertificateTemplateSubjectNameFlag
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CertEnroll.h
api_name:
 - X509CertificateTemplateSubjectNameFlag
---

# X509CertificateTemplateSubjectNameFlag enumeration


## -description

The <b>X509CertificateTemplateSubjectNameFlag</b> enumeration contains values that specify server and client actions concerning subject names.

## -enum-fields

### -field SubjectNameEnrolleeSupplies:0x1

Instructs the client to provide subject information in the certificate request.

### -field SubjectNameRequireDirectoryPath:0x80000000

Instructs the certification authority (CA) to specify the requestor's Active Directory distinguished name as the subject name in the issued certificate.

### -field SubjectNameRequireCommonName:0x40000000

Instructs the certification authority (CA) to specify the requestor's Active Directory common name (CN) as the subject name in the issued certificate.

### -field SubjectNameRequireEmail:0x20000000

Instructs the CA to specify the value of the <b>e-mail</b> attribute in the requestor's Active Directory user object as the subject name in the issued certificate.

### -field SubjectNameRequireDNS:0x10000000

Instructs the CA to specify the value of the <b>DNS</b> attribute in the requestor's Active Directory user object as the subject name in the issued certificate.

### -field SubjectNameAndAlternativeNameOldCertSupplies:0x8

Instructs the client to reuse the subject name and alternative subject name extensions from an existing valid certificate when creating a renewal certificate request.  This flag can only be used when the <b>SubjectNameEnrolleeSupplies</b> or the <b>SubjectAlternativeNameEnrolleeSupplies</b> flag is specified.

### -field SubjectAlternativeNameEnrolleeSupplies:0x10000

Instructs the client to provide subject alternative name information in the certificate request.

### -field SubjectAlternativeNameRequireDirectoryGUID:0x1000000

Instructs the CA to add the value of the <b>objectGUID </b> attribute in the requestor's Active Directory user object to the Subject Alternative Name extension in the issued certificate.

### -field SubjectAlternativeNameRequireUPN:0x2000000

Instructs the CA to add the value of the <b>UPN</b> attribute in the requestor's Active Directory user object to the Subject Alternative Name extension in the issued certificate.

### -field SubjectAlternativeNameRequireEmail:0x4000000

Instructs the CA to add the value of the <b>e-mail</b> attribute in the requestor's Active Directory user object to the Subject Alternative Name extension in the issued certificate.

### -field SubjectAlternativeNameRequireSPN:0x800000

Instructs the CA to add the value of the <b>SPN</b> attribute in the requestor's Active Directory user object to the Subject Alternative Name extension in the issued certificate.

### -field SubjectAlternativeNameRequireDNS:0x8000000

Instructs the CA to add the value of the <b>DNS</b> attribute in the requestor's Active Directory user object to the Subject Alternative Name extension  in the issued certificate.

### -field SubjectAlternativeNameRequireDomainDNS:0x400000

Instructs the CA to add the value of the DNS of the root domain to the Subject Alternative Name extension  in the issued certificate.


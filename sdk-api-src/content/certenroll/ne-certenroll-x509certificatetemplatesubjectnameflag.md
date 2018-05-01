---
UID: NE:certenroll.X509CertificateTemplateSubjectNameFlag
title: X509CertificateTemplateSubjectNameFlag
author: windows-driver-content
description: Contains values that specify server and client actions concerning subject names.
old-location: security\x509certificatetemplatesubjectnameflag.htm
old-project: SecCertEnroll
ms.assetid: 0880bb94-d26f-49a7-9749-f8be272fa4f6
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: SubjectAlternativeNameEnrolleeSupplies, SubjectAlternativeNameRequireDNS, SubjectAlternativeNameRequireDirectoryGUID, SubjectAlternativeNameRequireDomainDNS, SubjectAlternativeNameRequireEmail, SubjectAlternativeNameRequireSPN, SubjectAlternativeNameRequireUPN, SubjectNameAndAlternativeNameOldCertSupplies, SubjectNameEnrolleeSupplies, SubjectNameRequireCommonName, SubjectNameRequireDNS, SubjectNameRequireDirectoryPath, SubjectNameRequireEmail, X509CertificateTemplateSubjectNameFlag, X509CertificateTemplateSubjectNameFlag enumeration [Security], certenroll/SubjectAlternativeNameEnrolleeSupplies, certenroll/SubjectAlternativeNameRequireDNS, certenroll/SubjectAlternativeNameRequireDirectoryGUID, certenroll/SubjectAlternativeNameRequireDomainDNS, certenroll/SubjectAlternativeNameRequireEmail, certenroll/SubjectAlternativeNameRequireSPN, certenroll/SubjectAlternativeNameRequireUPN, certenroll/SubjectNameAndAlternativeNameOldCertSupplies, certenroll/SubjectNameEnrolleeSupplies, certenroll/SubjectNameRequireCommonName, certenroll/SubjectNameRequireDNS, certenroll/SubjectNameRequireDirectoryPath, certenroll/SubjectNameRequireEmail, certenroll/X509CertificateTemplateSubjectNameFlag, security.x509certificatetemplatesubjectnameflag
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: X509CertificateTemplateSubjectNameFlag
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	CertEnroll.h
api_name:
-	X509CertificateTemplateSubjectNameFlag
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
---

# X509CertificateTemplateSubjectNameFlag enumeration


## -description


The <b>X509CertificateTemplateSubjectNameFlag</b> enumeration contains values that specify server and client actions concerning subject names.


## -enum-fields




### -field SubjectNameEnrolleeSupplies

Instructs the client to provide subject information in the certificate request.


### -field SubjectNameRequireDirectoryPath

Instructs the certification authority (CA) to specify the requestor's Active Directory distinguished name as the subject name in the issued certificate.


### -field SubjectNameRequireCommonName

Instructs the certification authority (CA) to specify the requestor's Active Directory common name (CN) as the subject name in the issued certificate.


### -field SubjectNameRequireEmail

Instructs the CA to specify the value of the <b>e-mail</b> attribute in the requestor's Active Directory user object as the subject name in the issued certificate.


### -field SubjectNameRequireDNS

Instructs the CA to specify the value of the <b>DNS</b> attribute in the requestor's Active Directory user object as the subject name in the issued certificate.


### -field SubjectNameAndAlternativeNameOldCertSupplies

Instructs the client to reuse the subject name and alternative subject name extensions from an existing valid certificate when creating a renewal certificate request.  This flag can only be used when the <b>SubjectNameEnrolleeSupplies</b> or the <b>SubjectAlternativeNameEnrolleeSupplies</b> flag is specified.


### -field SubjectAlternativeNameEnrolleeSupplies

Instructs the client to provide subject alternative name information in the certificate request.


### -field SubjectAlternativeNameRequireDirectoryGUID

Instructs the CA to add the value of the <b>objectGUID </b> attribute in the requestor's Active Directory user object to the Subject Alternative Name extension in the issued certificate.


### -field SubjectAlternativeNameRequireUPN

Instructs the CA to add the value of the <b>UPN</b> attribute in the requestor's Active Directory user object to the Subject Alternative Name extension in the issued certificate.


### -field SubjectAlternativeNameRequireEmail

Instructs the CA to add the value of the <b>e-mail</b> attribute in the requestor's Active Directory user object to the Subject Alternative Name extension in the issued certificate.


### -field SubjectAlternativeNameRequireSPN

Instructs the CA to add the value of the <b>SPN</b> attribute in the requestor's Active Directory user object to the Subject Alternative Name extension in the issued certificate.


### -field SubjectAlternativeNameRequireDNS

Instructs the CA to add the value of the <b>DNS</b> attribute in the requestor's Active Directory user object to the Subject Alternative Name extension  in the issued certificate.


### -field SubjectAlternativeNameRequireDomainDNS

Instructs the CA to add the value of the DNS of the root domain to the Subject Alternative Name extension  in the issued certificate.


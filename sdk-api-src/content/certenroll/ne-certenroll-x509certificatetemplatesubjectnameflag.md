---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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


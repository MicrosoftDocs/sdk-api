---
UID: NE:certenroll.EnrollmentCAProperty
title: EnrollmentCAProperty
author: windows-sdk-content
description: Specifies certification authority property values.
old-location: security\enrollmentcaproperty.htm
tech.root: seccertenroll
ms.assetid: d4908ef0-aaf0-4396-9b89-cd7f3a9f6188
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CAPropCertificate, CAPropCertificateTypes, CAPropCommonName, CAPropDNSName, CAPropDescription, CAPropDistinguishedName, CAPropRenewalOnly, CAPropSanitizedName, CAPropSanitizedShortName, CAPropSecurity, CAPropSiteName, CAPropWebServers, EnrollmentCAProperty, EnrollmentCAProperty enumeration [Security], certenroll/CAPropCertificate, certenroll/CAPropCertificateTypes, certenroll/CAPropCommonName, certenroll/CAPropDNSName, certenroll/CAPropDescription, certenroll/CAPropDistinguishedName, certenroll/CAPropRenewalOnly, certenroll/CAPropSanitizedName, certenroll/CAPropSanitizedShortName, certenroll/CAPropSecurity, certenroll/CAPropSiteName, certenroll/CAPropWebServers, certenroll/EnrollmentCAProperty, security.enrollmentcaproperty
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Certenroll.h
api_name:
 - EnrollmentCAProperty
product: Windows
targetos: Windows
req.typenames: EnrollmentCAProperty
req.redist: 
---

# EnrollmentCAProperty enumeration


## -description


The <b>EnrollmentCAProperty</b> enumeration specifies certification authority property values. It is used by the <a href="https://msdn.microsoft.com/02f2d6bf-9290-43e1-ae44-a21325c176b2">Property</a> method on the <a href="https://msdn.microsoft.com/ffd64396-a258-4cf5-aca1-a61102ecf313">ICertificationAuthority</a> interface.


## -enum-fields




### -field CAPropCommonName

A <b>VT_BSTR</b> value that contains the common name of the certification authority (CA) in Active Directory.


### -field CAPropDistinguishedName

A <b>VT_DISPATCH</b> value that contains a pointer to an <a href="https://msdn.microsoft.com/49f176d9-33f6-4bc1-992c-c613279b0969">IX500DistinguishedName</a> object.


### -field CAPropSanitizedName

A <b>VT_BSTR</b> value that contains the sanitized common  name of the CA in Active Directory. A name is sanitized by replacing disallowed characters with an exclamation point (!) followed by four hexadecimal values that represent the character.


### -field CAPropSanitizedShortName

A <b>VT_BSTR</b> value that contains the sanitized and shortened common  name of the CA in Active Directory. A name is sanitized by replacing disallowed characters with an exclamation point (!) followed by four hexadecimal values that represent the character. The name is then shortened so that it does not exceed 51 characters. The characters that are removed from the sanitized string must be hashed and the hash converted to a 5-character string.


### -field CAPropDNSName

A <b>VT_BSTR</b> value that contains the DNS  name of the CA in Active Directory.


### -field CAPropCertificateTypes

A <b>VT_ARRAY|VT_BSTR</b> collection of templates supported by the CA.


### -field CAPropCertificate

A <b>VT_ARRAY | VT_UI1</b> value that contains the signing certificate used by the CA.	


### -field CAPropDescription

A <b>VT_BSTR</b> value that contains a description comment for the CA.


### -field CAPropWebServers

A <b>VT_ARRAY|VT_BSTR</b> collection of certificate enrollment servers configured for the CA. Each string in the collection contains a server URL, the authentication method used, an integer that specifies the priority level, and an integer that specifies whether the server can perform only certificate renewals. Each value is delimited by a newline character.


### -field CAPropSiteName

A <b>VT_BSTR</b> value that contains the name of the AD site to which the CA belongs. This can be used by the enrolling clients to determine the relative cost of communicating with the CA versus CAs that belong to other sites. This value is relevant only for CA objects retrieved by using the <a href="https://msdn.microsoft.com/37836fd1-e95a-4025-b268-f78a9113e568">GetCAs</a> method on the <a href="https://msdn.microsoft.com/e39d40fd-3d43-4cdc-b41a-07a87a11bfad">IX509EnrollmentPolicyServer</a> interface.


### -field CAPropSecurity

A <b>VT_BSTR</b> value that contains the security descriptor definition language (SDDL) string representation of the security descriptor for the CA. This value is relevant only for CA objects retrieved by using the <a href="https://msdn.microsoft.com/37836fd1-e95a-4025-b268-f78a9113e568">GetCAs</a> method.


### -field CAPropRenewalOnly

A <b>VT_BOOL</b> value that specifies whether a CA is configured to perform only certificate renewals. This value is relevant only for CA objects retrieved by using the <a href="https://msdn.microsoft.com/37836fd1-e95a-4025-b268-f78a9113e568">GetCAs</a> method.


## -see-also




<a href="https://msdn.microsoft.com/ffd64396-a258-4cf5-aca1-a61102ecf313">ICertificationAuthority</a>



<a href="https://msdn.microsoft.com/02f2d6bf-9290-43e1-ae44-a21325c176b2">Property</a>
 

 


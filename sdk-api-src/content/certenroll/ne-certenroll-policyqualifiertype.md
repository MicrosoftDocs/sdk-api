---
UID: NE:certenroll.PolicyQualifierType
title: PolicyQualifierType
author: windows-sdk-content
description: Specifies the type of qualifier applied to a certificate policy.
old-location: security\policyqualifiertype_enum.htm
tech.root: SecCertEnroll
ms.assetid: 76cd1874-b80d-466e-9c7d-12cf8d310b8a
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: PolicyQualifierType, PolicyQualifierType enumeration [Security], PolicyQualifierTypeUnknown, PolicyQualifierTypeUrl, PolicyQualifierTypeUserNotice, certenroll/PolicyQualifierType, certenroll/PolicyQualifierTypeUnknown, certenroll/PolicyQualifierTypeUrl, certenroll/PolicyQualifierTypeUserNotice, security.policyqualifiertype_enum
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - CertEnroll.h
api_name:
 - PolicyQualifierType
product: Windows
targetos: Windows
req.typenames: PolicyQualifierType
req.redist: 
---

# PolicyQualifierType enumeration


## -description


The <b>PolicyQualifierType</b> enumeration type specifies the type of qualifier applied to a <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certificate policy</a>. This enumeration is used by the <a href="https://msdn.microsoft.com/en-us/library/Aa376813(v=VS.85).aspx">InitializeEncode</a> method and the  <a href="https://msdn.microsoft.com/en-us/library/Aa376819(v=VS.85).aspx">Type</a> property on the <a href="https://msdn.microsoft.com/en-us/library/Aa376803(v=VS.85).aspx">IPolicyQualifier</a> interface. 


## -enum-fields




### -field PolicyQualifierTypeUnknown

The qualifier type is not specified.


### -field PolicyQualifierTypeUrl

The qualifier is a URL that points to a Certification Practice Statement (CPS) that has been defined by the <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certification authority</a> to outline the policies under which the <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certificate</a> was issued and the purposes for which the certificate can be used.


### -field PolicyQualifierTypeUserNotice

The qualifier is a text statement to be displayed by the application to any user who relies on the certificate. The user notice identifies the permitted uses of the certificate.


### -field PolicyQualifierTypeFlags




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa374846(v=VS.85).aspx">CertEnroll Enumerations</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa376803(v=VS.85).aspx">IPolicyQualifier</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa376804(v=VS.85).aspx">IPolicyQualifiers</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa378121(v=VS.85).aspx">IX509ExtensionCertificatePolicies</a>
 

 


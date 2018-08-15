---
UID: NE:certenroll.PolicyQualifierType
title: PolicyQualifierType
author: windows-sdk-content
description: Specifies the type of qualifier applied to a certificate policy.
old-location: security\policyqualifiertype_enum.htm
old-project: seccertenroll
ms.assetid: 76cd1874-b80d-466e-9c7d-12cf8d310b8a
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: PolicyQualifierType, PolicyQualifierType enumeration [Security], PolicyQualifierTypeUnknown, PolicyQualifierTypeUrl, PolicyQualifierTypeUserNotice, certenroll/PolicyQualifierType, certenroll/PolicyQualifierTypeUnknown, certenroll/PolicyQualifierTypeUrl, certenroll/PolicyQualifierTypeUserNotice, security.policyqualifiertype_enum
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: certenroll.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: PolicyQualifierType
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
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
---

# PolicyQualifierType enumeration


## -description


The <b>PolicyQualifierType</b> enumeration type specifies the type of qualifier applied to a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate policy</a>. This enumeration is used by the <a href="https://msdn.microsoft.com/fc8b5916-0557-4f9b-8478-169a3dd9cebc">InitializeEncode</a> method and the  <a href="https://msdn.microsoft.com/eb48d2a0-c689-45b1-9f06-83df71987b4b">Type</a> property on the <a href="https://msdn.microsoft.com/3804e372-17bb-458d-8da5-85d760fe5e60">IPolicyQualifier</a> interface. 


## -enum-fields




### -field PolicyQualifierTypeUnknown

The qualifier type is not specified.


### -field PolicyQualifierTypeUrl

The qualifier is a URL that points to a Certification Practice Statement (CPS) that has been defined by the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> to outline the policies under which the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate</a> was issued and the purposes for which the certificate can be used.


### -field PolicyQualifierTypeUserNotice

The qualifier is a text statement to be displayed by the application to any user who relies on the certificate. The user notice identifies the permitted uses of the certificate.


### -field PolicyQualifierTypeFlags




## -see-also




<a href="https://msdn.microsoft.com/8514fb89-1cf5-4e09-997c-17984efc4e03">CertEnroll Enumerations</a>



<a href="https://msdn.microsoft.com/3804e372-17bb-458d-8da5-85d760fe5e60">IPolicyQualifier</a>



<a href="https://msdn.microsoft.com/da8b6289-379e-4dff-b15a-b0967f245c3d">IPolicyQualifiers</a>



<a href="https://msdn.microsoft.com/d35d155c-fb81-4d7e-b5c9-82ac5af4b79e">IX509ExtensionCertificatePolicies</a>
 

 


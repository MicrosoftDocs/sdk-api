---
UID: NF:certenroll.IX509CertificateRequest.put_SuppressDefaults
title: IX509CertificateRequest::put_SuppressDefaults
author: windows-sdk-content
description: Specifies or retrieves a Boolean value that indicates whether the default extensions and attributes are included in the request.
old-location: security\ix509certificaterequest_suppressdefaults_property.htm
old-project: seccertenroll
ms.assetid: 3a7847b6-52b4-4058-8113-cbc3b9101a5b
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IX509CertificateRequest interface [Security],SuppressDefaults property, IX509CertificateRequest.SuppressDefaults, IX509CertificateRequest.put_SuppressDefaults, IX509CertificateRequest::SuppressDefaults, IX509CertificateRequest::get_SuppressDefaults, IX509CertificateRequest::put_SuppressDefaults, SuppressDefaults property [Security], SuppressDefaults property [Security],IX509CertificateRequest interface, certenroll/IX509CertificateRequest::SuppressDefaults, certenroll/IX509CertificateRequest::get_SuppressDefaults, certenroll/IX509CertificateRequest::put_SuppressDefaults, put_SuppressDefaults, security.ix509certificaterequest_suppressdefaults_property
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: X509RequestType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509CertificateRequest.SuppressDefaults
 - IX509CertificateRequest.get_SuppressDefaults
 - IX509CertificateRequest.put_SuppressDefaults
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509CertificateRequest::put_SuppressDefaults


## -description


The <b>SuppressDefaults</b> property specifies or retrieves a Boolean value that indicates whether the default extensions and attributes are included in the request. The defaults are represented by their <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifiers</a> (OIDs).

This property is read/write.


## -parameters


## -remarks



You must initialize the request object before calling this property. Set this property before calling the <a href="https://msdn.microsoft.com/098788f4-539f-420b-a4e1-65625dd56ca1">Encode</a> method to suppress inclusion and encoding of default extensions and attributes in the certificate request.




## -see-also




<a href="https://msdn.microsoft.com/5425c9ab-565d-449d-87e1-e5765868acfb">IX509CertificateRequest</a>



<a href="https://msdn.microsoft.com/7197a225-b2dc-47bb-8843-d3fb4bf95811">IX509CertificateRequestCertificate</a>



<a href="https://msdn.microsoft.com/77059388-c442-4db5-ab27-1db25e2f63b9">IX509CertificateRequestCmc</a>



<a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a>



<a href="https://msdn.microsoft.com/ae869557-6523-4387-835e-c9631898d864">IX509CertificateRequestPkcs7</a>



<a href="https://msdn.microsoft.com/25774ccb-8e76-443d-89da-177d6e77c019">IX509SignatureInformation</a>
 

 


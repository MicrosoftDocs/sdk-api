---
UID: NF:certenroll.IX509CertificateRequest.get_RawData
title: IX509CertificateRequest::get_RawData
author: windows-sdk-content
description: Retrieves a byte array that contains the signed, Distinguished Encoding Rules (DER) encoded certificate request.
old-location: security\ix509certificaterequest_rawdata_property.htm
tech.root: SecCertEnroll
ms.assetid: 1830a569-03a4-4692-adbf-b627bf4370a1
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IX509CertificateRequest interface [Security],RawData property, IX509CertificateRequest.RawData, IX509CertificateRequest.get_RawData, IX509CertificateRequest::RawData, IX509CertificateRequest::get_RawData, RawData property [Security], RawData property [Security],IX509CertificateRequest interface, certenroll/IX509CertificateRequest::RawData, certenroll/IX509CertificateRequest::get_RawData, get_RawData, security.ix509certificaterequest_rawdata_property
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509CertificateRequest.RawData
 - IX509CertificateRequest.get_RawData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- certenroll.h
: 
- IX509CertificateRequest.get_RawData
: 
---

# IX509CertificateRequest::get_RawData


## -description


The <b>RawData</b> property retrieves a byte array that contains the signed, <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) encoded certificate request. The byte array is represented by a Unicode-encoded string.

This property is read-only.


## -parameters


## -remarks



Call the <a href="https://msdn.microsoft.com/098788f4-539f-420b-a4e1-65625dd56ca1">Encode</a> method to encode a certificate request using DER as defined by the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) standard. The encoding process creates a byte array that the <b>RawData</b> property returns   as a string. The string is either a pure binary sequence, or it is Unicode encoded so that it can be displayed as text. 




## -see-also




<a href="https://msdn.microsoft.com/5425c9ab-565d-449d-87e1-e5765868acfb">IX509CertificateRequest</a>



<a href="https://msdn.microsoft.com/7197a225-b2dc-47bb-8843-d3fb4bf95811">IX509CertificateRequestCertificate</a>



<a href="https://msdn.microsoft.com/77059388-c442-4db5-ab27-1db25e2f63b9">IX509CertificateRequestCmc</a>



<a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a>



<a href="https://msdn.microsoft.com/ae869557-6523-4387-835e-c9631898d864">IX509CertificateRequestPkcs7</a>



<a href="https://msdn.microsoft.com/25774ccb-8e76-443d-89da-177d6e77c019">IX509SignatureInformation</a>
 

 


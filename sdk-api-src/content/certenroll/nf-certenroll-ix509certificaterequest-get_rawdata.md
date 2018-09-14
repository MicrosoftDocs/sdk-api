---
UID: NF:certenroll.IX509CertificateRequest.get_RawData
title: IX509CertificateRequest::get_RawData
author: windows-sdk-content
description: Retrieves a byte array that contains the signed, Distinguished Encoding Rules (DER) encoded certificate request.
old-location: security\ix509certificaterequest_rawdata_property.htm
tech.root: seccertenroll
ms.assetid: 1830a569-03a4-4692-adbf-b627bf4370a1
ms.author: windowssdkdev
ms.date: 08/31/2018
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
---

# IX509CertificateRequest::get_RawData


## -description


The <b>RawData</b> property retrieves a byte array that contains the signed, <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Distinguished Encoding Rules</a> (DER) encoded certificate request. The byte array is represented by a Unicode-encoded string.

This property is read-only.


## -parameters


## -remarks



Call the <a href="https://msdn.microsoft.com/en-us/library/Aa377650(v=VS.85).aspx">Encode</a> method to encode a certificate request using DER as defined by the <a href="https://msdn.microsoft.com/en-us/library/ms721532(v=VS.85).aspx">Abstract Syntax Notation One</a> (ASN.1) standard. The encoding process creates a byte array that the <b>RawData</b> property returns   as a string. The string is either a pure binary sequence, or it is Unicode encoded so that it can be displayed as text. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa377123(v=VS.85).aspx">IX509CertificateRequest</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377124(v=VS.85).aspx">IX509CertificateRequestCertificate</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377133(v=VS.85).aspx">IX509CertificateRequestCmc</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377505(v=VS.85).aspx">IX509CertificateRequestPkcs10</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377608(v=VS.85).aspx">IX509CertificateRequestPkcs7</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa379050(v=VS.85).aspx">IX509SignatureInformation</a>
 

 


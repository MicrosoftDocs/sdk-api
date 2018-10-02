---
UID: NF:certenroll.IX509CertificateRequest.get_HashAlgorithm
title: IX509CertificateRequest::get_HashAlgorithm
author: windows-sdk-content
description: Specifies and retrieves the object identifier (OID) of the hash algorithm used to sign the certificate request.
old-location: security\ix509certificaterequest_hashalgorithm_property.htm
tech.root: SecCertEnroll
ms.assetid: 9f68ee54-5dea-47bb-8a90-0285d081c9b8
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: HashAlgorithm property [Security], HashAlgorithm property [Security],IX509CertificateRequest interface, IX509CertificateRequest interface [Security],HashAlgorithm property, IX509CertificateRequest.HashAlgorithm, IX509CertificateRequest.get_HashAlgorithm, IX509CertificateRequest::HashAlgorithm, IX509CertificateRequest::get_HashAlgorithm, IX509CertificateRequest::put_HashAlgorithm, certenroll/IX509CertificateRequest::HashAlgorithm, certenroll/IX509CertificateRequest::get_HashAlgorithm, certenroll/IX509CertificateRequest::put_HashAlgorithm, get_HashAlgorithm, security.ix509certificaterequest_hashalgorithm_property
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
 - IX509CertificateRequest.HashAlgorithm
 - IX509CertificateRequest.get_HashAlgorithm
 - IX509CertificateRequest.put_HashAlgorithm
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509CertificateRequest::get_HashAlgorithm


## -description


The <b>HashAlgorithm</b> property specifies and retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a> (OID) of the hash algorithm used to sign the certificate request. This property is web enabled for both input and output.

This property is read/write.


## -parameters


## -remarks



If the certificate request contains nested requests and you set the <b>HashAlgorithm</b> property on the top level request, it is automatically propagated to all of the inner requests, overwriting values that may have been previously set. You can, however, set the property manually on each of the inner objects.

You must initialize the request object before calling this property. You can call this property before calling the <a href="https://msdn.microsoft.com/en-us/library/Aa377650(v=VS.85).aspx">Encode</a> method.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa377123(v=VS.85).aspx">IX509CertificateRequest</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377124(v=VS.85).aspx">IX509CertificateRequestCertificate</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377133(v=VS.85).aspx">IX509CertificateRequestCmc</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377505(v=VS.85).aspx">IX509CertificateRequestPkcs10</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377608(v=VS.85).aspx">IX509CertificateRequestPkcs7</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa379050(v=VS.85).aspx">IX509SignatureInformation</a>
 

 


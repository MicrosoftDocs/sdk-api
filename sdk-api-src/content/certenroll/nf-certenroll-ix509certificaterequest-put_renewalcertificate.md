---
UID: NF:certenroll.IX509CertificateRequest.put_RenewalCertificate
title: IX509CertificateRequest::put_RenewalCertificate
author: windows-sdk-content
description: Specifies or retrieves a byte array that contains the Distinguished Encoding Rules (DER) encoded certificate that is being renewed.
old-location: security\ix509certificaterequest_renewalcertificate_property.htm
tech.root: SecCertEnroll
ms.assetid: ab046b65-a059-4b48-a6cd-7e2f0b18bc65
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IX509CertificateRequest interface [Security],RenewalCertificate property, IX509CertificateRequest.RenewalCertificate, IX509CertificateRequest.put_RenewalCertificate, IX509CertificateRequest::RenewalCertificate, IX509CertificateRequest::get_RenewalCertificate, IX509CertificateRequest::put_RenewalCertificate, RenewalCertificate property [Security], RenewalCertificate property [Security],IX509CertificateRequest interface, certenroll/IX509CertificateRequest::RenewalCertificate, certenroll/IX509CertificateRequest::get_RenewalCertificate, certenroll/IX509CertificateRequest::put_RenewalCertificate, put_RenewalCertificate, security.ix509certificaterequest_renewalcertificate_property
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
 - IX509CertificateRequest.RenewalCertificate
 - IX509CertificateRequest.get_RenewalCertificate
 - IX509CertificateRequest.put_RenewalCertificate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509CertificateRequest::put_RenewalCertificate


## -description


The <b>RenewalCertificate</b> property specifies or retrieves a byte array that contains the <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Distinguished Encoding Rules</a> (DER) encoded certificate that is being renewed.  The DER-encoded byte array is represented by a Unicode-encoded string.

This property is read/write.


## -parameters


## -remarks



The certificate is encoded by using DER as defined by the <a href="https://msdn.microsoft.com/en-us/library/ms721532(v=VS.85).aspx">Abstract Syntax Notation One</a> (ASN.1) standard. The encoding process creates a byte array. The byte array is returned in a  string that is either a pure binary sequence or is Unicode encoded so that it can be displayed as text.

You must initialize the request object before calling this property. You can call this property before calling the <a href="https://msdn.microsoft.com/en-us/library/Aa377650(v=VS.85).aspx">Encode</a> method.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa377123(v=VS.85).aspx">IX509CertificateRequest</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377124(v=VS.85).aspx">IX509CertificateRequestCertificate</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377133(v=VS.85).aspx">IX509CertificateRequestCmc</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377505(v=VS.85).aspx">IX509CertificateRequestPkcs10</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377608(v=VS.85).aspx">IX509CertificateRequestPkcs7</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa379050(v=VS.85).aspx">IX509SignatureInformation</a>
 

 


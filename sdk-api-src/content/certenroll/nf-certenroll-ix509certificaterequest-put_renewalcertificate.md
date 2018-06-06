---
UID: NF:certenroll.IX509CertificateRequest.put_RenewalCertificate
title: IX509CertificateRequest::put_RenewalCertificate
author: windows-sdk-content
description: Specifies or retrieves a byte array that contains the Distinguished Encoding Rules (DER) encoded certificate that is being renewed.
old-location: security\ix509certificaterequest_renewalcertificate_property.htm
old-project: SecCertEnroll
ms.assetid: ab046b65-a059-4b48-a6cd-7e2f0b18bc65
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IX509CertificateRequest interface [Security],RenewalCertificate property, IX509CertificateRequest.RenewalCertificate, IX509CertificateRequest.put_RenewalCertificate, IX509CertificateRequest::RenewalCertificate, IX509CertificateRequest::get_RenewalCertificate, IX509CertificateRequest::put_RenewalCertificate, RenewalCertificate property [Security], RenewalCertificate property [Security],IX509CertificateRequest interface, certenroll/IX509CertificateRequest::RenewalCertificate, certenroll/IX509CertificateRequest::get_RenewalCertificate, certenroll/IX509CertificateRequest::put_RenewalCertificate, put_RenewalCertificate, security.ix509certificaterequest_renewalcertificate_property
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
 - IX509CertificateRequest.RenewalCertificate
 - IX509CertificateRequest.get_RenewalCertificate
 - IX509CertificateRequest.put_RenewalCertificate
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509CertificateRequest::put_RenewalCertificate


## -description


The <b>RenewalCertificate</b> property specifies or retrieves a byte array that contains the <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) encoded certificate that is being renewed.  The DER-encoded byte array is represented by a Unicode-encoded string.

This property is read/write.


## -parameters


## -remarks



The certificate is encoded by using DER as defined by the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) standard. The encoding process creates a byte array. The byte array is returned in a  string that is either a pure binary sequence or is Unicode encoded so that it can be displayed as text.

You must initialize the request object before calling this property. You can call this property before calling the <a href="https://msdn.microsoft.com/098788f4-539f-420b-a4e1-65625dd56ca1">Encode</a> method.




## -see-also




<a href="https://msdn.microsoft.com/5425c9ab-565d-449d-87e1-e5765868acfb">IX509CertificateRequest</a>



<a href="https://msdn.microsoft.com/7197a225-b2dc-47bb-8843-d3fb4bf95811">IX509CertificateRequestCertificate</a>



<a href="https://msdn.microsoft.com/77059388-c442-4db5-ab27-1db25e2f63b9">IX509CertificateRequestCmc</a>



<a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a>



<a href="https://msdn.microsoft.com/ae869557-6523-4387-835e-c9631898d864">IX509CertificateRequestPkcs7</a>



<a href="https://msdn.microsoft.com/25774ccb-8e76-443d-89da-177d6e77c019">IX509SignatureInformation</a>
 

 


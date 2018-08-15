---
UID: NF:certenroll.IX509CertificateRequestCertificate.put_SerialNumber
title: IX509CertificateRequestCertificate::put_SerialNumber
author: windows-sdk-content
description: Specifies and retrieves the certificate serial number.
old-location: security\ix509certificaterequestcertificate_serialnumber_property.htm
old-project: seccertenroll
ms.assetid: ab9d576d-bca2-4388-97ee-9c409c0084c5
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IX509CertificateRequestCertificate interface [Security],SerialNumber property, IX509CertificateRequestCertificate.SerialNumber, IX509CertificateRequestCertificate.put_SerialNumber, IX509CertificateRequestCertificate::SerialNumber, IX509CertificateRequestCertificate::get_SerialNumber, IX509CertificateRequestCertificate::put_SerialNumber, SerialNumber property [Security], SerialNumber property [Security],IX509CertificateRequestCertificate interface, certenroll/IX509CertificateRequestCertificate::SerialNumber, certenroll/IX509CertificateRequestCertificate::get_SerialNumber, certenroll/IX509CertificateRequestCertificate::put_SerialNumber, put_SerialNumber, security.ix509certificaterequestcertificate_serialnumber_property
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: X509RequestType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509CertificateRequestCertificate.SerialNumber
 - IX509CertificateRequestCertificate.get_SerialNumber
 - IX509CertificateRequestCertificate.put_SerialNumber
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509CertificateRequestCertificate::put_SerialNumber


## -description


The <b>SerialNumber</b> property specifies and retrieves the certificate serial number. The serial number is contained in a byte array  encoded by using <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) as defined by the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) standard.  The DER-encoded byte array is represented by  a string that is either a pure binary sequence or is Unicode encoded.   

This property is read/write.


## -parameters


## -remarks



After calling <a href="https://msdn.microsoft.com/098788f4-539f-420b-a4e1-65625dd56ca1">Encode</a>, the default value is a GUID with a high-order nibble that is not zero (to ensure that the hexadecimal representation of the serial number has an even number of digits). The high-order nibble is in the range 1 to 7. You must initialize the request object before calling this property. For more information, see any of the following methods:<ul>
<li>
<a href="https://msdn.microsoft.com/be0e2cda-5481-49ab-9a12-6dc52981fd24">Initialize</a>
</li>
<li>
<a href="https://msdn.microsoft.com/10ab62c3-9c6f-4e1b-8a86-131d08282d9c">InitializeDecode</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3f390abc-5c1c-4f9c-a5f4-4d6fec065acf">InitializeFromCertificate</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b26e69c4-bfe4-4395-aaf6-bc1d045f59cc">InitializeFromPrivateKey</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7b7e00dc-649b-4bcb-a9b6-5745b33ea48b">InitializeFromPublicKey</a>
</li>
<li>
<a href="https://msdn.microsoft.com/4ea746c3-b967-41b4-94ae-7b16b93ca4e4">InitializeFromTemplateName</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/7197a225-b2dc-47bb-8843-d3fb4bf95811">IX509CertificateRequestCertificate</a>
 

 


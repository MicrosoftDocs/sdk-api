---
UID: NF:certenroll.IX509CertificateRequestCertificate.put_SerialNumber
title: IX509CertificateRequestCertificate::put_SerialNumber
author: windows-sdk-content
description: Specifies and retrieves the certificate serial number.
old-location: security\ix509certificaterequestcertificate_serialnumber_property.htm
tech.root: SecCertEnroll
ms.assetid: ab9d576d-bca2-4388-97ee-9c409c0084c5
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IX509CertificateRequestCertificate interface [Security],SerialNumber property, IX509CertificateRequestCertificate.SerialNumber, IX509CertificateRequestCertificate.put_SerialNumber, IX509CertificateRequestCertificate::SerialNumber, IX509CertificateRequestCertificate::get_SerialNumber, IX509CertificateRequestCertificate::put_SerialNumber, SerialNumber property [Security], SerialNumber property [Security],IX509CertificateRequestCertificate interface, certenroll/IX509CertificateRequestCertificate::SerialNumber, certenroll/IX509CertificateRequestCertificate::get_SerialNumber, certenroll/IX509CertificateRequestCertificate::put_SerialNumber, put_SerialNumber, security.ix509certificaterequestcertificate_serialnumber_property
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
 - IX509CertificateRequestCertificate.SerialNumber
 - IX509CertificateRequestCertificate.get_SerialNumber
 - IX509CertificateRequestCertificate.put_SerialNumber
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
- IX509CertificateRequestCertificate.put_SerialNumber
: 
---

# IX509CertificateRequestCertificate::put_SerialNumber


## -description


The <b>SerialNumber</b> property specifies and retrieves the certificate serial number. The serial number is contained in a byte array  encoded by using <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Distinguished Encoding Rules</a> (DER) as defined by the <a href="https://msdn.microsoft.com/en-us/library/ms721532(v=VS.85).aspx">Abstract Syntax Notation One</a> (ASN.1) standard.  The DER-encoded byte array is represented by  a string that is either a pure binary sequence or is Unicode encoded.   

This property is read/write.


## -parameters


## -remarks



After calling <a href="https://msdn.microsoft.com/en-us/library/Aa377650(v=VS.85).aspx">Encode</a>, the default value is a GUID with a high-order nibble that is not zero (to ensure that the hexadecimal representation of the serial number has an even number of digits). The high-order nibble is in the range 1 to 7. You must initialize the request object before calling this property. For more information, see any of the following methods:<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377669(v=VS.85).aspx">Initialize</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377520(v=VS.85).aspx">InitializeDecode</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377523(v=VS.85).aspx">InitializeFromCertificate</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377527(v=VS.85).aspx">InitializeFromPrivateKey</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377531(v=VS.85).aspx">InitializeFromPublicKey</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377533(v=VS.85).aspx">InitializeFromTemplateName</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa377124(v=VS.85).aspx">IX509CertificateRequestCertificate</a>
 

 


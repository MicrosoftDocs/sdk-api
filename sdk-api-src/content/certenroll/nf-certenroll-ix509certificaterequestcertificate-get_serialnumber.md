---
UID: NF:certenroll.IX509CertificateRequestCertificate.get_SerialNumber
title: IX509CertificateRequestCertificate::get_SerialNumber (certenroll.h)
description: Specifies and retrieves the certificate serial number. (Get)
helpviewer_keywords: ["IX509CertificateRequestCertificate interface [Security]","SerialNumber property","IX509CertificateRequestCertificate.SerialNumber","IX509CertificateRequestCertificate.get_SerialNumber","IX509CertificateRequestCertificate::SerialNumber","IX509CertificateRequestCertificate::get_SerialNumber","IX509CertificateRequestCertificate::put_SerialNumber","SerialNumber property [Security]","SerialNumber property [Security]","IX509CertificateRequestCertificate interface","certenroll/IX509CertificateRequestCertificate::SerialNumber","certenroll/IX509CertificateRequestCertificate::get_SerialNumber","certenroll/IX509CertificateRequestCertificate::put_SerialNumber","get_SerialNumber","security.ix509certificaterequestcertificate_serialnumber_property"]
old-location: security\ix509certificaterequestcertificate_serialnumber_property.htm
tech.root: security
ms.assetid: ab9d576d-bca2-4388-97ee-9c409c0084c5
ms.date: 12/05/2018
ms.keywords: IX509CertificateRequestCertificate interface [Security],SerialNumber property, IX509CertificateRequestCertificate.SerialNumber, IX509CertificateRequestCertificate.get_SerialNumber, IX509CertificateRequestCertificate::SerialNumber, IX509CertificateRequestCertificate::get_SerialNumber, IX509CertificateRequestCertificate::put_SerialNumber, SerialNumber property [Security], SerialNumber property [Security],IX509CertificateRequestCertificate interface, certenroll/IX509CertificateRequestCertificate::SerialNumber, certenroll/IX509CertificateRequestCertificate::get_SerialNumber, certenroll/IX509CertificateRequestCertificate::put_SerialNumber, get_SerialNumber, security.ix509certificaterequestcertificate_serialnumber_property
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IX509CertificateRequestCertificate::get_SerialNumber
 - certenroll/IX509CertificateRequestCertificate::get_SerialNumber
dev_langs:
 - c++
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
---

# IX509CertificateRequestCertificate::get_SerialNumber


## -description

The <b>SerialNumber</b> property specifies and retrieves the certificate serial number. The serial number is contained in a byte array  encoded by using <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) as defined by the <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) standard.  The DER-encoded byte array is represented by  a string that is either a pure binary sequence or is Unicode encoded.   

This property is read/write.

## -parameters

## -remarks

After calling <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-encode">Encode</a>, the default value is a GUID with a high-order nibble that is not zero (to ensure that the hexadecimal representation of the serial number has an even number of digits). The high-order nibble is in the range 1 to 7. You must initialize the request object before calling this property. For more information, see any of the following methods:<ul>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-initialize">Initialize</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializedecode">InitializeDecode</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromcertificate">InitializeFromCertificate</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromprivatekey">InitializeFromPrivateKey</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializefrompublickey">InitializeFromPublicKey</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromtemplatename">InitializeFromTemplateName</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcertificate">IX509CertificateRequestCertificate</a>

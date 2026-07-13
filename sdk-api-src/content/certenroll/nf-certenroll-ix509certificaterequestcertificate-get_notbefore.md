---
UID: NF:certenroll.IX509CertificateRequestCertificate.get_NotBefore
title: IX509CertificateRequestCertificate::get_NotBefore (certenroll.h)
description: Specifies or retrieves the date and time before which the certificate is not valid. (Get)
helpviewer_keywords: ["IX509CertificateRequestCertificate interface [Security]","NotBefore property","IX509CertificateRequestCertificate.NotBefore","IX509CertificateRequestCertificate.get_NotBefore","IX509CertificateRequestCertificate::NotBefore","IX509CertificateRequestCertificate::get_NotBefore","IX509CertificateRequestCertificate::put_NotBefore","NotBefore property [Security]","NotBefore property [Security]","IX509CertificateRequestCertificate interface","certenroll/IX509CertificateRequestCertificate::NotBefore","certenroll/IX509CertificateRequestCertificate::get_NotBefore","certenroll/IX509CertificateRequestCertificate::put_NotBefore","get_NotBefore","security.ix509certificaterequestcertificate_notbefore_property"]
old-location: security\ix509certificaterequestcertificate_notbefore_property.htm
tech.root: security
ms.assetid: 2568df97-6864-452d-aa18-a5ee47956abd
ms.date: 12/05/2018
ms.keywords: IX509CertificateRequestCertificate interface [Security],NotBefore property, IX509CertificateRequestCertificate.NotBefore, IX509CertificateRequestCertificate.get_NotBefore, IX509CertificateRequestCertificate::NotBefore, IX509CertificateRequestCertificate::get_NotBefore, IX509CertificateRequestCertificate::put_NotBefore, NotBefore property [Security], NotBefore property [Security],IX509CertificateRequestCertificate interface, certenroll/IX509CertificateRequestCertificate::NotBefore, certenroll/IX509CertificateRequestCertificate::get_NotBefore, certenroll/IX509CertificateRequestCertificate::put_NotBefore, get_NotBefore, security.ix509certificaterequestcertificate_notbefore_property
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
 - IX509CertificateRequestCertificate::get_NotBefore
 - certenroll/IX509CertificateRequestCertificate::get_NotBefore
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
 - IX509CertificateRequestCertificate.NotBefore
 - IX509CertificateRequestCertificate.get_NotBefore
 - IX509CertificateRequestCertificate.put_NotBefore
---

# IX509CertificateRequestCertificate::get_NotBefore


## -description

The <b>NotBefore</b> property specifies or retrieves the date and time before which the certificate is not valid.

This property is read/write.

## -parameters

## -remarks

The expiration date is stored as an 8-byte real value that represents a Coordinated Universal Time (Greenwich Mean Time) value between January 1, 1900 and December 31, 9999, inclusive. The value 2.0 represents January 1, 1900; 3.0 represents January 2, 1900. Adding 1 to the value increments the date by a day. The fractional part of the value represents the time of day. Therefore, 2.5 represents 12:00 on January 1, 1900; 3.25 represents 06:00 on January 2, 1900.

For dates between 1950 and 2049 inclusive, the date and time is encoded Coordinated Universal Time in the form YYMMDDHHMMSS. For dates before 1950 or after 2049, encoded generalized time is used. Encoded generalized time is in the form YYYYMMDDHHMMSSMMM, using a four digit year, and is precise to milliseconds. The <b>NotBefore</b> time is, however, only precise to seconds.

After calling <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-encode">Encode</a>, the default value equals the current time plus one year minus ten minutes to compensate for clock skew. Typically, this value is adjusted by time zone and daylight saving time, if applicable, before it is displayed.

You must initialize the request object before calling this property. For more information, see any of the following methods:<ul>
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

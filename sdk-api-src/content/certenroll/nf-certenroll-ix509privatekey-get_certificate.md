---
UID: NF:certenroll.IX509PrivateKey.get_Certificate
title: IX509PrivateKey::get_Certificate (certenroll.h)
description: Specifies or retrieves a byte array that contains the certificate associated with the private key. (Get)
helpviewer_keywords: ["Certificate property [Security]","Certificate property [Security]","IX509PrivateKey interface","IX509PrivateKey interface [Security]","Certificate property","IX509PrivateKey.Certificate","IX509PrivateKey.get_Certificate","IX509PrivateKey::Certificate","IX509PrivateKey::get_Certificate","IX509PrivateKey::put_Certificate","certenroll/IX509PrivateKey::Certificate","certenroll/IX509PrivateKey::get_Certificate","certenroll/IX509PrivateKey::put_Certificate","get_Certificate","security.ix509privatekey_certificate_property"]
old-location: security\ix509privatekey_certificate_property.htm
tech.root: security
ms.assetid: 035615f1-2dc7-47d7-98e4-7b5b0924030f
ms.date: 12/05/2018
ms.keywords: Certificate property [Security], Certificate property [Security],IX509PrivateKey interface, IX509PrivateKey interface [Security],Certificate property, IX509PrivateKey.Certificate, IX509PrivateKey.get_Certificate, IX509PrivateKey::Certificate, IX509PrivateKey::get_Certificate, IX509PrivateKey::put_Certificate, certenroll/IX509PrivateKey::Certificate, certenroll/IX509PrivateKey::get_Certificate, certenroll/IX509PrivateKey::put_Certificate, get_Certificate, security.ix509privatekey_certificate_property
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
 - IX509PrivateKey::get_Certificate
 - certenroll/IX509PrivateKey::get_Certificate
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
 - IX509PrivateKey.Certificate
 - IX509PrivateKey.get_Certificate
 - IX509PrivateKey.put_Certificate
---

# IX509PrivateKey::get_Certificate


## -description

The <b>Certificate</b> property specifies or retrieves a byte array that contains the certificate associated with the private key.  The byte array is represented by a Unicode-encoded string.

This property is read/write.

## -parameters

## -remarks

If the key is not open when you specify a  certificate, the certificate will be set when the key is opened. For more information, see the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-open">Open</a> method.

The <b>Certificate</b> property compares the public key associated with the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a> object to the public key included in the certificate. The two keys must match.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a>

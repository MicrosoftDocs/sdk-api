---
UID: NF:certenroll.IX509PrivateKey.put_KeyUsage
title: IX509PrivateKey::put_KeyUsage (certenroll.h)
description: Specifies or retrieves a value that identifies the specific purpose for which a private key can be used. (Put)
helpviewer_keywords: ["IX509PrivateKey interface [Security]","KeyUsage property","IX509PrivateKey.KeyUsage","IX509PrivateKey.put_KeyUsage","IX509PrivateKey::KeyUsage","IX509PrivateKey::get_KeyUsage","IX509PrivateKey::put_KeyUsage","KeyUsage property [Security]","KeyUsage property [Security]","IX509PrivateKey interface","certenroll/IX509PrivateKey::KeyUsage","certenroll/IX509PrivateKey::get_KeyUsage","certenroll/IX509PrivateKey::put_KeyUsage","put_KeyUsage","security.ix509privatekey_keyusage"]
old-location: security\ix509privatekey_keyusage.htm
tech.root: security
ms.assetid: e983c95b-6b3a-4e27-8a23-ef9051b11a16
ms.date: 12/05/2018
ms.keywords: IX509PrivateKey interface [Security],KeyUsage property, IX509PrivateKey.KeyUsage, IX509PrivateKey.put_KeyUsage, IX509PrivateKey::KeyUsage, IX509PrivateKey::get_KeyUsage, IX509PrivateKey::put_KeyUsage, KeyUsage property [Security], KeyUsage property [Security],IX509PrivateKey interface, certenroll/IX509PrivateKey::KeyUsage, certenroll/IX509PrivateKey::get_KeyUsage, certenroll/IX509PrivateKey::put_KeyUsage, put_KeyUsage, security.ix509privatekey_keyusage
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
 - IX509PrivateKey::put_KeyUsage
 - certenroll/IX509PrivateKey::put_KeyUsage
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
 - IX509PrivateKey.KeyUsage
 - IX509PrivateKey.get_KeyUsage
 - IX509PrivateKey.put_KeyUsage
---

# IX509PrivateKey::put_KeyUsage


## -description

The <b>KeyUsage</b> property specifies or retrieves a  value that identifies the specific purpose for which a private key can be used. This property is web enabled for both input and output.

This property is read/write.

## -parameters

## -remarks

If you set the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_keyspec">KeySpec</a> property for a  legacy CSP to XCN_NCRYPT_ALLOW_SIGNING_FLAG, the <b>KeyUsage</b> property to XCN_NCRYPT_ALLOW_SIGNING_FLAG. If you specify XCN_AT_KEYEXCHANGE, the <b>KeyUsage</b> property is automatically set to XCN_NCRYPT_ALLOW_DECRYPT_FLAG |
             XCN_NCRYPT_ALLOW_KEY_AGREEMENT_FLAG.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a>

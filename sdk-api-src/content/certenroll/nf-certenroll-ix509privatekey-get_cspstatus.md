---
UID: NF:certenroll.IX509PrivateKey.get_CspStatus
title: IX509PrivateKey::get_CspStatus (certenroll.h)
description: Specifies or retrieves an ICspStatus object that contains information about the cryptographic provider and algorithm pair associated with the private key. (Get)
helpviewer_keywords: ["CspStatus property [Security]","CspStatus property [Security]","IX509PrivateKey interface","IX509PrivateKey interface [Security]","CspStatus property","IX509PrivateKey.CspStatus","IX509PrivateKey.get_CspStatus","IX509PrivateKey::CspStatus","IX509PrivateKey::get_CspStatus","IX509PrivateKey::put_CspStatus","certenroll/IX509PrivateKey::CspStatus","certenroll/IX509PrivateKey::get_CspStatus","certenroll/IX509PrivateKey::put_CspStatus","get_CspStatus","security.ix509privatekey_cspstatus"]
old-location: security\ix509privatekey_cspstatus.htm
tech.root: security
ms.assetid: 8bf6e62d-9ecf-4eee-9652-f04d2010b4f7
ms.date: 12/05/2018
ms.keywords: CspStatus property [Security], CspStatus property [Security],IX509PrivateKey interface, IX509PrivateKey interface [Security],CspStatus property, IX509PrivateKey.CspStatus, IX509PrivateKey.get_CspStatus, IX509PrivateKey::CspStatus, IX509PrivateKey::get_CspStatus, IX509PrivateKey::put_CspStatus, certenroll/IX509PrivateKey::CspStatus, certenroll/IX509PrivateKey::get_CspStatus, certenroll/IX509PrivateKey::put_CspStatus, get_CspStatus, security.ix509privatekey_cspstatus
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
 - IX509PrivateKey::get_CspStatus
 - certenroll/IX509PrivateKey::get_CspStatus
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
 - IX509PrivateKey.CspStatus
 - IX509PrivateKey.get_CspStatus
 - IX509PrivateKey.put_CspStatus
---

# IX509PrivateKey::get_CspStatus


## -description

The <b>CspStatus</b> property specifies or retrieves an <a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatus">ICspStatus</a> object that contains information about the cryptographic provider and algorithm pair associated with the private key. This property is web enabled for both input and output.

This property is read/write.

## -parameters

## -remarks

The <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_algorithm">Algorithm</a> and <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_providername">ProviderName</a> properties are automatically set when you call the <b>CspStatus</b> property. The <b>CspStatus</b> property is typically set during the enrollment process. That is, when a request template specifies multiple provider/algorithm pairs, the enrollment code sets the <b>CspStatus</b> property to the first enabled <a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatus">ICspStatus</a> object and tries to create a private key. If a key cannot be created, the enrollment code sets this property to the next enabled <b>ICspStatus</b> object and tries again.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a>

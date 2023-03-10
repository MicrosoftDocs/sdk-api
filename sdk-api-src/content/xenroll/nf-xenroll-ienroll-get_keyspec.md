---
UID: NF:xenroll.IEnroll.get_KeySpec
title: IEnroll::get_KeySpec (xenroll.h)
description: Sets or retrieves the type of key generated. (Get)
helpviewer_keywords: ["IEnroll interface [Security]","KeySpec property","IEnroll.KeySpec","IEnroll.get_KeySpec","IEnroll::KeySpec","IEnroll::get_KeySpec","IEnroll::put_KeySpec","KeySpec property [Security]","KeySpec property [Security]","IEnroll interface","get_KeySpec","security.ienroll4_keyspec","xenroll/IEnroll::KeySpec","xenroll/IEnroll::get_KeySpec","xenroll/IEnroll::put_KeySpec"]
old-location: security\ienroll4_keyspec.htm
tech.root: security
ms.assetid: b05851a0-6228-44e4-9bd7-354c862596e2
ms.date: 12/05/2018
ms.keywords: IEnroll interface [Security],KeySpec property, IEnroll.KeySpec, IEnroll.get_KeySpec, IEnroll::KeySpec, IEnroll::get_KeySpec, IEnroll::put_KeySpec, KeySpec property [Security], KeySpec property [Security],IEnroll interface, get_KeySpec, security.ienroll4_keyspec, xenroll/IEnroll::KeySpec, xenroll/IEnroll::get_KeySpec, xenroll/IEnroll::put_KeySpec
req.header: xenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnroll::get_KeySpec
 - xenroll/IEnroll::get_KeySpec
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - IEnroll.KeySpec
 - IEnroll.get_KeySpec
 - IEnroll.put_KeySpec
---

# IEnroll::get_KeySpec


## -description

<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>KeySpec</b> property sets or retrieves the  type of key generated.

 Valid values are determined by the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) in use. This property was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll">IEnroll</a> interface.

This property is read/write.

## -parameters

## -remarks

For the Microsoft Base Cryptographic Provider, the <b>KeySpec</b> property has a value of AT_KEYEXCHANGE for <a href="/windows/desktop/SecGloss/e-gly">exchange keys</a>, or AT_SIGNATURE for signature keys. The default is AT_SIGNATURE.

For information about the other Microsoft CSPs, see 
<a href="/windows/desktop/SecCrypto/cryptographic-service-providers">Cryptographic Service Providers</a> in the CryptoAPI 2.0 documentation.

For information about other CSPs, see the documentation provided with the CSP.


The <b>KeySpec</b> property affects the behavior of the following methods:

<ul>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-createpkcs10wstr">createPKCS10WStr</a>
</li>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-createfilepkcs10wstr">createFilePKCS10WStr</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll</a>

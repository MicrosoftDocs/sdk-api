---
UID: NF:xenroll.IEnroll.get_GenKeyFlags
title: IEnroll::get_GenKeyFlags (xenroll.h)
description: Sets or retrieves the values passed to CryptGenKey when the certificate request is generated. (Get)
helpviewer_keywords: ["GenKeyFlags property [Security]","GenKeyFlags property [Security]","IEnroll interface","IEnroll interface [Security]","GenKeyFlags property","IEnroll.GenKeyFlags","IEnroll.get_GenKeyFlags","IEnroll::GenKeyFlags","IEnroll::get_GenKeyFlags","IEnroll::put_GenKeyFlags","get_GenKeyFlags","security.ienroll4_genkeyflags","xenroll/IEnroll::GenKeyFlags","xenroll/IEnroll::get_GenKeyFlags","xenroll/IEnroll::put_GenKeyFlags"]
old-location: security\ienroll4_genkeyflags.htm
tech.root: security
ms.assetid: 6dac3321-9dca-4b7d-8432-e8124bd51db7
ms.date: 12/05/2018
ms.keywords: GenKeyFlags property [Security], GenKeyFlags property [Security],IEnroll interface, IEnroll interface [Security],GenKeyFlags property, IEnroll.GenKeyFlags, IEnroll.get_GenKeyFlags, IEnroll::GenKeyFlags, IEnroll::get_GenKeyFlags, IEnroll::put_GenKeyFlags, get_GenKeyFlags, security.ienroll4_genkeyflags, xenroll/IEnroll::GenKeyFlags, xenroll/IEnroll::get_GenKeyFlags, xenroll/IEnroll::put_GenKeyFlags
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
 - IEnroll::get_GenKeyFlags
 - xenroll/IEnroll::get_GenKeyFlags
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
 - IEnroll.GenKeyFlags
 - IEnroll.get_GenKeyFlags
 - IEnroll.put_GenKeyFlags
---

# IEnroll::get_GenKeyFlags


## -description

<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>GenKeyFlags</b> property sets or retrieves the values passed to <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenkey">CryptGenKey</a> when the certificate request is generated.

By default, the <b>GenKeyFlags</b> property is set to zero. However, when a .pvk file is specified, the value of <b>GenKeyFlags</b> defaults to CRYPT_EXPORTABLE. For more information, see Remarks.

This property was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll">IEnroll</a> interface.

This property is read/write.

## -parameters

## -remarks

By default, private keys are not exportable unless a .pvk file is requested. To make the private key exportable without specifying a .pvk file, set <b>GenKeyFlags</b> to CRYPT_EXPORTABLE.

To specify a .pvk file name,  use the 
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_pvkfilenamewstr">PVKFileNameWStr</a> property.

The <b>GenKeyFlags</b> property value is passed to the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenkey">CryptGenKey</a> CryptoAPI function by using its <i>dwFlags</i> parameter.

If the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a>  (CSP) does not support exportable private keys, an error occurs.


The <b>GenKeyFlags</b> property affects the behavior of the following methods:

<ul>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-createpkcs10wstr">createPKCS10WStr</a>
</li>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-createfilepkcs10wstr">createFilePKCS10WStr</a>
</li>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createrequestwstr">createRequestWStr</a>
</li>
</ul>


<div class="alert"><b>Note</b>  The default value for the <b>GenKeyFlags</b> property is zero. If you need to change this value, you must do so before calling these methods. After calling any of these methods, you cannot change the <b>GenKeyFlags</b> property value.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenkey">CryptGenKey</a>



<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll</a>

---
UID: NF:xenroll.IEnroll.get_ProviderFlags
title: IEnroll::get_ProviderFlags (xenroll.h)
description: The ProviderFlags property of IEnroll4 sets or retrieves the provider type. (Get)
helpviewer_keywords: ["IEnroll interface [Security]","ProviderFlags property","IEnroll.ProviderFlags","IEnroll.get_ProviderFlags","IEnroll::ProviderFlags","IEnroll::get_ProviderFlags","IEnroll::put_ProviderFlags","ProviderFlags property [Security]","ProviderFlags property [Security]","IEnroll interface","get_ProviderFlags","security.ienroll4_providerflags","xenroll/IEnroll::ProviderFlags","xenroll/IEnroll::get_ProviderFlags","xenroll/IEnroll::put_ProviderFlags"]
old-location: security\ienroll4_providerflags.htm
tech.root: security
ms.assetid: 57e6f86e-fbd3-4fd7-acdd-146a67045ff8
ms.date: 12/05/2018
ms.keywords: IEnroll interface [Security],ProviderFlags property, IEnroll.ProviderFlags, IEnroll.get_ProviderFlags, IEnroll::ProviderFlags, IEnroll::get_ProviderFlags, IEnroll::put_ProviderFlags, ProviderFlags property [Security], ProviderFlags property [Security],IEnroll interface, get_ProviderFlags, security.ienroll4_providerflags, xenroll/IEnroll::ProviderFlags, xenroll/IEnroll::get_ProviderFlags, xenroll/IEnroll::put_ProviderFlags
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
 - IEnroll::get_ProviderFlags
 - xenroll/IEnroll::get_ProviderFlags
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
 - IEnroll.ProviderFlags
 - IEnroll.get_ProviderFlags
 - IEnroll.put_ProviderFlags
---

# IEnroll::get_ProviderFlags


## -description

<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>ProviderFlags</b> property  sets or retrieves the provider type.

The <b>ProviderFlags</b> property is passed to the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a> CryptoAPI function. Valid values are determined by the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) in use.

The default value for this property is zero. This property was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll">IEnroll</a> interface.

This property is read/write.

## -parameters

## -remarks

For  more information about   valid <b>ProviderFlags</b> values for the Microsoft Base Cryptographic Provider, see the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a> CryptoAPI function.

For information about  other CSPs, see the documentation provided with the CSP.

The <b>ProviderFlags</b> property value is passed to <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a>  by using  its <i>dwFlags</i> parameter.


The <b>ProviderFlags</b> property affects the behavior of the following methods:

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

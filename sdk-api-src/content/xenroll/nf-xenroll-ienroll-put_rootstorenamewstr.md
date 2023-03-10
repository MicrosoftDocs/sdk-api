---
UID: NF:xenroll.IEnroll.put_RootStoreNameWStr
title: IEnroll::put_RootStoreNameWStr (xenroll.h)
description: The RootStoreNameWStr property of IEnroll4 sets or retrieves the name of the root store where all intrinsically trusted, self-signed root certificates are kept. (Put)
helpviewer_keywords: ["IEnroll interface [Security]","RootStoreNameWStr property","IEnroll.RootStoreNameWStr","IEnroll.put_RootStoreNameWStr","IEnroll::RootStoreNameWStr","IEnroll::get_RootStoreNameWStr","IEnroll::put_RootStoreNameWStr","RootStoreNameWStr property [Security]","RootStoreNameWStr property [Security]","IEnroll interface","put_RootStoreNameWStr","security.ienroll4_rootstorenamewstr","xenroll/IEnroll::RootStoreNameWStr","xenroll/IEnroll::get_RootStoreNameWStr","xenroll/IEnroll::put_RootStoreNameWStr"]
old-location: security\ienroll4_rootstorenamewstr.htm
tech.root: security
ms.assetid: d1b60ba4-974e-43d4-a8f9-8ca619d6b878
ms.date: 12/05/2018
ms.keywords: IEnroll interface [Security],RootStoreNameWStr property, IEnroll.RootStoreNameWStr, IEnroll.put_RootStoreNameWStr, IEnroll::RootStoreNameWStr, IEnroll::get_RootStoreNameWStr, IEnroll::put_RootStoreNameWStr, RootStoreNameWStr property [Security], RootStoreNameWStr property [Security],IEnroll interface, put_RootStoreNameWStr, security.ienroll4_rootstorenamewstr, xenroll/IEnroll::RootStoreNameWStr, xenroll/IEnroll::get_RootStoreNameWStr, xenroll/IEnroll::put_RootStoreNameWStr
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
 - IEnroll::put_RootStoreNameWStr
 - xenroll/IEnroll::put_RootStoreNameWStr
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
 - IEnroll.RootStoreNameWStr
 - IEnroll.get_RootStoreNameWStr
 - IEnroll.put_RootStoreNameWStr
---

# IEnroll::put_RootStoreNameWStr


## -description

<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>RootStoreNameWStr</b> property sets or retrieves the name of the root store where all intrinsically trusted, self-signed <a href="/windows/desktop/SecGloss/r-gly">root certificates</a> are kept.

 The default value for this property is "ROOT". Because of the level of trust associated with the root store, the user may be prompted (by means of the user interface) to accept the certificate. Although this property need not be changed for many applications, to avoid the user interface associated with trusting <a href="/windows/desktop/SecGloss/r-gly">root certificates</a>, a possibility is to set <b>RootStoreNameWStr</b> to "CA".

This property was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll">IEnroll</a> interface.

This property is read/write.

## -parameters

## -remarks

<b>RootStoreNameWStr</b> affects the behavior of the following methods:

<ul>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-acceptpkcs7blob">acceptPKCS7Blob</a>
</li>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-acceptfilepkcs7wstr">acceptFilePKCS7WStr</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll</a>

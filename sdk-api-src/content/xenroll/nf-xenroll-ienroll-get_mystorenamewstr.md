---
UID: NF:xenroll.IEnroll.get_MyStoreNameWStr
title: IEnroll::get_MyStoreNameWStr (xenroll.h)
description: The MyStoreNameWStr property of IEnroll4 sets or retrieves the name of the store where certificates with linked private keys are kept. (Get)
helpviewer_keywords: ["IEnroll interface [Security]","MyStoreNameWStr property","IEnroll.MyStoreNameWStr","IEnroll.get_MyStoreNameWStr","IEnroll::MyStoreNameWStr","IEnroll::get_MyStoreNameWStr","IEnroll::put_MyStoreNameWStr","MyStoreNameWStr property [Security]","MyStoreNameWStr property [Security]","IEnroll interface","get_MyStoreNameWStr","security.ienroll4_mystorenamewstr","xenroll/IEnroll::MyStoreNameWStr","xenroll/IEnroll::get_MyStoreNameWStr","xenroll/IEnroll::put_MyStoreNameWStr"]
old-location: security\ienroll4_mystorenamewstr.htm
tech.root: security
ms.assetid: 077bc593-0071-4f41-8d07-141c9959b6ed
ms.date: 12/05/2018
ms.keywords: IEnroll interface [Security],MyStoreNameWStr property, IEnroll.MyStoreNameWStr, IEnroll.get_MyStoreNameWStr, IEnroll::MyStoreNameWStr, IEnroll::get_MyStoreNameWStr, IEnroll::put_MyStoreNameWStr, MyStoreNameWStr property [Security], MyStoreNameWStr property [Security],IEnroll interface, get_MyStoreNameWStr, security.ienroll4_mystorenamewstr, xenroll/IEnroll::MyStoreNameWStr, xenroll/IEnroll::get_MyStoreNameWStr, xenroll/IEnroll::put_MyStoreNameWStr
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
 - IEnroll::get_MyStoreNameWStr
 - xenroll/IEnroll::get_MyStoreNameWStr
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
 - IEnroll.MyStoreNameWStr
 - IEnroll.get_MyStoreNameWStr
 - IEnroll.put_MyStoreNameWStr
---

# IEnroll::get_MyStoreNameWStr


## -description

<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>MyStoreNameWStr</b> property  sets or retrieves the name of the store  where certificates with linked <a href="/windows/desktop/SecGloss/p-gly">private keys</a> are kept.

The value of <b>MyStoreNameWStr</b> specifies the store in which to place the new certificate produced from 
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-acceptpkcs7blob">acceptPKCS7Blob</a> or 
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-acceptfilepkcs7wstr">acceptFilePKCS7WStr</a>. The default value for this property is "MY". This property was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll">IEnroll</a> interface.

This property is read/write.

## -parameters

## -remarks

The <b>MyStoreNameWStr</b> property affects the behavior of the following methods:

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

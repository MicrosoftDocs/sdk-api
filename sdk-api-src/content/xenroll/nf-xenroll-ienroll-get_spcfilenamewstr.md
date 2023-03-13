---
UID: NF:xenroll.IEnroll.get_SPCFileNameWStr
title: IEnroll::get_SPCFileNameWStr (xenroll.h)
description: The SPCFileNameWStr property of IEnroll4 sets or retrieves the name of the file to which to write the base64-encoded PKCS (Get)
helpviewer_keywords: ["IEnroll interface [Security]","SPCFileNameWStr property","IEnroll.SPCFileNameWStr","IEnroll.get_SPCFileNameWStr","IEnroll::SPCFileNameWStr","IEnroll::get_SPCFileNameWStr","IEnroll::put_SPCFileNameWStr","SPCFileNameWStr property [Security]","SPCFileNameWStr property [Security]","IEnroll interface","get_SPCFileNameWStr","security.ienroll4_spcfilenamewstr","xenroll/IEnroll::SPCFileNameWStr","xenroll/IEnroll::get_SPCFileNameWStr","xenroll/IEnroll::put_SPCFileNameWStr"]
old-location: security\ienroll4_spcfilenamewstr.htm
tech.root: security
ms.assetid: 75e9327e-72d6-4247-a339-1ca494bc8408
ms.date: 12/05/2018
ms.keywords: IEnroll interface [Security],SPCFileNameWStr property, IEnroll.SPCFileNameWStr, IEnroll.get_SPCFileNameWStr, IEnroll::SPCFileNameWStr, IEnroll::get_SPCFileNameWStr, IEnroll::put_SPCFileNameWStr, SPCFileNameWStr property [Security], SPCFileNameWStr property [Security],IEnroll interface, get_SPCFileNameWStr, security.ienroll4_spcfilenamewstr, xenroll/IEnroll::SPCFileNameWStr, xenroll/IEnroll::get_SPCFileNameWStr, xenroll/IEnroll::put_SPCFileNameWStr
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
 - IEnroll::get_SPCFileNameWStr
 - xenroll/IEnroll::get_SPCFileNameWStr
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
 - IEnroll.SPCFileNameWStr
 - IEnroll.get_SPCFileNameWStr
 - IEnroll.put_SPCFileNameWStr
---

# IEnroll::get_SPCFileNameWStr


## -description

<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>SPCFileNameWStr</b> property sets or retrieves the name of the file to which to write the base64-encoded PKCS #7 (in <b>BSTR</b> form) as returned from the <a href="/windows/desktop/SecGloss/c-gly">certification authority</a>.

This property was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll">IEnroll</a> interface.

This property is read/write.

## -parameters

## -remarks

The file is written as a binary PKCS #7. Specifying this file does not affect the acceptance of the certificates into any of the user's stores.

If the file already exists, the user is notified and prompted for permission to overwrite it.


<b>SPCFileNameWStr</b> affects the behavior of the following methods:

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

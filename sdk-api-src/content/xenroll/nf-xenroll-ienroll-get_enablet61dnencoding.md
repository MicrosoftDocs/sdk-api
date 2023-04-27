---
UID: NF:xenroll.IEnroll.get_EnableT61DNEncoding
title: IEnroll::get_EnableT61DNEncoding (xenroll.h)
description: Sets or retrieves a Boolean value that determines whether the distinguished name in the request is encoded as a T61 string instead of as a Unicode string. (Get)
helpviewer_keywords: ["EnableT61DNEncoding property [Security]","EnableT61DNEncoding property [Security]","IEnroll interface","IEnroll interface [Security]","EnableT61DNEncoding property","IEnroll.EnableT61DNEncoding","IEnroll.get_EnableT61DNEncoding","IEnroll::EnableT61DNEncoding","IEnroll::get_EnableT61DNEncoding","IEnroll::put_EnableT61DNEncoding","get_EnableT61DNEncoding","security.ienroll4_enablet61dnencoding","xenroll/IEnroll::EnableT61DNEncoding","xenroll/IEnroll::get_EnableT61DNEncoding","xenroll/IEnroll::put_EnableT61DNEncoding"]
old-location: security\ienroll4_enablet61dnencoding.htm
tech.root: security
ms.assetid: 7ed181d1-b06f-40f4-892a-80edf327bf40
ms.date: 12/05/2018
ms.keywords: EnableT61DNEncoding property [Security], EnableT61DNEncoding property [Security],IEnroll interface, IEnroll interface [Security],EnableT61DNEncoding property, IEnroll.EnableT61DNEncoding, IEnroll.get_EnableT61DNEncoding, IEnroll::EnableT61DNEncoding, IEnroll::get_EnableT61DNEncoding, IEnroll::put_EnableT61DNEncoding, get_EnableT61DNEncoding, security.ienroll4_enablet61dnencoding, xenroll/IEnroll::EnableT61DNEncoding, xenroll/IEnroll::get_EnableT61DNEncoding, xenroll/IEnroll::put_EnableT61DNEncoding
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
 - IEnroll::get_EnableT61DNEncoding
 - xenroll/IEnroll::get_EnableT61DNEncoding
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
 - IEnroll.EnableT61DNEncoding
 - IEnroll.get_EnableT61DNEncoding
 - IEnroll.put_EnableT61DNEncoding
---

# IEnroll::get_EnableT61DNEncoding


## -description

<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>EnableT61DNEncoding</b> property sets or retrieves a Boolean value that determines whether the distinguished name in the request is encoded as a T61 string instead of as a <a href="/windows/desktop/SecGloss/u-gly">Unicode</a> string.

 A T61 character is 8 bits, hence all <a href="/windows/desktop/SecGloss/u-gly">Unicode</a> characters to be encoded must be less than or equal to 0xFF.  This property was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll2">IEnroll2</a> interface.

This property is read/write.

## -parameters

## -remarks

The <b>EnableT61DNEncoding</b> property affects the behavior of the following methods:

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

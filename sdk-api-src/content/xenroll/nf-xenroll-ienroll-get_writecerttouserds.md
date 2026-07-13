---
UID: NF:xenroll.IEnroll.get_WriteCertToUserDS
title: IEnroll::get_WriteCertToUserDS (xenroll.h)
description: The WriteCertToUserDS property of IEnroll4 sets or retrieves a Boolean value that determines whether the certificate is written to the user's Active Directory store. (Get)
helpviewer_keywords: ["IEnroll interface [Security]","WriteCertToUserDS property","IEnroll.WriteCertToUserDS","IEnroll.get_WriteCertToUserDS","IEnroll::WriteCertToUserDS","IEnroll::get_WriteCertToUserDS","IEnroll::put_WriteCertToUserDS","WriteCertToUserDS property [Security]","WriteCertToUserDS property [Security]","IEnroll interface","get_WriteCertToUserDS","security.ienroll4_writecerttouserds","xenroll/IEnroll::WriteCertToUserDS","xenroll/IEnroll::get_WriteCertToUserDS","xenroll/IEnroll::put_WriteCertToUserDS"]
old-location: security\ienroll4_writecerttouserds.htm
tech.root: security
ms.assetid: 8b29f442-265f-4826-a2f0-3305d6f70cbb
ms.date: 12/05/2018
ms.keywords: IEnroll interface [Security],WriteCertToUserDS property, IEnroll.WriteCertToUserDS, IEnroll.get_WriteCertToUserDS, IEnroll::WriteCertToUserDS, IEnroll::get_WriteCertToUserDS, IEnroll::put_WriteCertToUserDS, WriteCertToUserDS property [Security], WriteCertToUserDS property [Security],IEnroll interface, get_WriteCertToUserDS, security.ienroll4_writecerttouserds, xenroll/IEnroll::WriteCertToUserDS, xenroll/IEnroll::get_WriteCertToUserDS, xenroll/IEnroll::put_WriteCertToUserDS
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
 - IEnroll::get_WriteCertToUserDS
 - xenroll/IEnroll::get_WriteCertToUserDS
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
 - IEnroll.WriteCertToUserDS
 - IEnroll.get_WriteCertToUserDS
 - IEnroll.put_WriteCertToUserDS
---

# IEnroll::get_WriteCertToUserDS


## -description

<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>WriteCertToUserDS</b> property sets or retrieves a Boolean value that determines whether the certificate is written to the user's Active Directory  store.

 This property should not need to be modified by most applications. This property was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll2">IEnroll2</a> interface.

This property is read/write.

## -parameters

## -remarks

<b>WriteCertToUserDS</b> affects the behavior of the following methods:

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

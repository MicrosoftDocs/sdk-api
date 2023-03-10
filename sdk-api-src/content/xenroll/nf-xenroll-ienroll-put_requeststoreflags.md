---
UID: NF:xenroll.IEnroll.put_RequestStoreFlags
title: IEnroll::put_RequestStoreFlags (xenroll.h)
description: The RequestStoreFlags property of IEnroll4 sets or retrieves the registry location used for the request store. (Put)
helpviewer_keywords: ["IEnroll interface [Security]","RequestStoreFlags property","IEnroll.RequestStoreFlags","IEnroll.put_RequestStoreFlags","IEnroll::RequestStoreFlags","IEnroll::get_RequestStoreFlags","IEnroll::put_RequestStoreFlags","RequestStoreFlags property [Security]","RequestStoreFlags property [Security]","IEnroll interface","put_RequestStoreFlags","security.ienroll4_requeststoreflags","xenroll/IEnroll::RequestStoreFlags","xenroll/IEnroll::get_RequestStoreFlags","xenroll/IEnroll::put_RequestStoreFlags"]
old-location: security\ienroll4_requeststoreflags.htm
tech.root: security
ms.assetid: 95ed42ed-04ff-482c-954c-a6c9dd9ccd4c
ms.date: 12/05/2018
ms.keywords: IEnroll interface [Security],RequestStoreFlags property, IEnroll.RequestStoreFlags, IEnroll.put_RequestStoreFlags, IEnroll::RequestStoreFlags, IEnroll::get_RequestStoreFlags, IEnroll::put_RequestStoreFlags, RequestStoreFlags property [Security], RequestStoreFlags property [Security],IEnroll interface, put_RequestStoreFlags, security.ienroll4_requeststoreflags, xenroll/IEnroll::RequestStoreFlags, xenroll/IEnroll::get_RequestStoreFlags, xenroll/IEnroll::put_RequestStoreFlags
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
 - IEnroll::put_RequestStoreFlags
 - xenroll/IEnroll::put_RequestStoreFlags
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
 - IEnroll.RequestStoreFlags
 - IEnroll.get_RequestStoreFlags
 - IEnroll.put_RequestStoreFlags
---

# IEnroll::put_RequestStoreFlags


## -description

<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>RequestStoreFlags</b> property sets or retrieves the registry location used for the request store.

 The default value for this property  is CERT_SYSTEM_STORE_CURRENT_USER. This property was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll">IEnroll</a> interface.

This property is read/write.

## -parameters

## -remarks

The <b>RequestStoreFlags</b> property value is passed to the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certopenstore">CertOpenStore</a> CryptoAPI function  by using its <i>dwFlags</i> parameter.

Typically, modification of the <b>RequestStoreFlags</b> property is  performed only in advanced applications.


The <b>RequestStoreFlags</b> property should be set before using the following methods:

<ul>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-acceptpkcs7blob">acceptPKCS7Blob</a>
</li>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-acceptfilepkcs7wstr">acceptFilePKCS7WStr</a>
</li>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-createpkcs10wstr">createPKCS10WStr</a>
</li>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-createfilepkcs10wstr">createFilePKCS10WStr</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll</a>

---
UID: NF:xenroll.IEnroll.get_RequestStoreTypeWStr
title: IEnroll::get_RequestStoreTypeWStr (xenroll.h)
description: Sets or retrieves the type of store to use for the store specified by the RequestStoreNameWStr property. This store type is passed directly to the CertOpenStore function. (Get)
helpviewer_keywords: ["IEnroll interface [Security]","RequestStoreTypeWStr property","IEnroll.RequestStoreTypeWStr","IEnroll.get_RequestStoreTypeWStr","IEnroll4 interface [Security]","RequestStoreTypeWStr property","IEnroll4.RequestStoreTypeWStr","IEnroll4::get_RequestStoreTypeWStr","IEnroll4::put_RequestStoreTypeWStr","IEnroll::RequestStoreTypeWStr","IEnroll::get_RequestStoreTypeWStr","IEnroll::put_RequestStoreTypeWStr","RequestStoreTypeWStr property [Security]","RequestStoreTypeWStr property [Security]","IEnroll interface","RequestStoreTypeWStr property [Security]","IEnroll4 interface","get_RequestStoreTypeWStr","put_RequestStoreTypeWStr","security.ienroll4_requeststoretypewstr","sz_CERT_STORE_PROV_SYSTEM_W","xenroll/IEnroll4::RequestStoreTypeWStr","xenroll/IEnroll4::get_RequestStoreTypeWStr","xenroll/IEnroll4::put_RequestStoreTypeWStr","xenroll/IEnroll::RequestStoreTypeWStr","xenroll/IEnroll::get_RequestStoreTypeWStr","xenroll/IEnroll::put_RequestStoreTypeWStr"]
old-location: security\ienroll4_requeststoretypewstr.htm
tech.root: security
ms.assetid: 5b06552a-7b8d-4044-9c2c-994f67e9c36d
ms.date: 12/05/2018
ms.keywords: IEnroll interface [Security],RequestStoreTypeWStr property, IEnroll.RequestStoreTypeWStr, IEnroll.get_RequestStoreTypeWStr, IEnroll4 interface [Security],RequestStoreTypeWStr property, IEnroll4.RequestStoreTypeWStr, IEnroll4::get_RequestStoreTypeWStr, IEnroll4::put_RequestStoreTypeWStr, IEnroll::RequestStoreTypeWStr, IEnroll::get_RequestStoreTypeWStr, IEnroll::put_RequestStoreTypeWStr, RequestStoreTypeWStr property [Security], RequestStoreTypeWStr property [Security],IEnroll interface, RequestStoreTypeWStr property [Security],IEnroll4 interface, get_RequestStoreTypeWStr, put_RequestStoreTypeWStr, security.ienroll4_requeststoretypewstr, sz_CERT_STORE_PROV_SYSTEM_W, xenroll/IEnroll4::RequestStoreTypeWStr, xenroll/IEnroll4::get_RequestStoreTypeWStr, xenroll/IEnroll4::put_RequestStoreTypeWStr, xenroll/IEnroll::RequestStoreTypeWStr, xenroll/IEnroll::get_RequestStoreTypeWStr, xenroll/IEnroll::put_RequestStoreTypeWStr
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
 - IEnroll::get_RequestStoreTypeWStr
 - xenroll/IEnroll::get_RequestStoreTypeWStr
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
 - IEnroll.RequestStoreTypeWStr
 - IEnroll.get_RequestStoreTypeWStr
 - IEnroll.put_RequestStoreTypeWStr
 - IEnroll4.RequestStoreTypeWStr
 - IEnroll4.get_RequestStoreTypeWStr
 - IEnroll4.put_RequestStoreTypeWStr
---

# IEnroll::get_RequestStoreTypeWStr


## -description

<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>RequestStoreTypeWStr</b> property sets or retrieves the type of store to use for the store specified by the 
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_requeststorenamewstr">RequestStoreNameWStr</a> property. This store type is passed directly  to the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certopenstore">CertOpenStore</a> function.

The default value of  this property is sz_CERT_STORE_PROV_SYSTEM. If the default is not to be used, this property must be set to the same value before calls to 
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-createpkcs10wstr">createPKCS10WStr</a> and 
				<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-createfilepkcs10wstr">createFilePKCS10WStr</a> and again before calls to 
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-acceptpkcs7blob">acceptPKCS7Blob</a> and 
				<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-acceptfilepkcs7wstr">acceptFilePKCS7WStr</a>.

Only system stores are supported. This property was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll">IEnroll</a> interface.

This property is read/write.

## -parameters

## -remarks

Typically, modification of the <b>RequestStoreTypeWStr</b> property is  performed only in advanced applications.


<b>RequestStoreTypeWStr</b> affects the behavior of the following methods:

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

<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll">IEnroll</a>



<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll4</a>

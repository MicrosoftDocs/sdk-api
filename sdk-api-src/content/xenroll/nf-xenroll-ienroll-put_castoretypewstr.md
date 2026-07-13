---
UID: NF:xenroll.IEnroll.put_CAStoreTypeWStr
title: IEnroll::put_CAStoreTypeWStr (xenroll.h)
description: Sets or retrieves the type of store to use for the store specified by the CAStoreNameWStr property. (Put)
helpviewer_keywords: ["CAStoreTypeWStr property [Security]","CAStoreTypeWStr property [Security]","IEnroll interface","IEnroll interface [Security]","CAStoreTypeWStr property","IEnroll.CAStoreTypeWStr","IEnroll.put_CAStoreTypeWStr","IEnroll::CAStoreTypeWStr","IEnroll::get_CAStoreTypeWStr","IEnroll::put_CAStoreTypeWStr","put_CAStoreTypeWStr","security.ienroll4_castoretypewstr","sz_CERT_STORE_PROV_SYSTEM_W","xenroll/IEnroll::CAStoreTypeWStr","xenroll/IEnroll::get_CAStoreTypeWStr","xenroll/IEnroll::put_CAStoreTypeWStr"]
old-location: security\ienroll4_castoretypewstr.htm
tech.root: security
ms.assetid: cbb60c1c-04ed-4477-bf8e-4dae9fd964ef
ms.date: 12/05/2018
ms.keywords: CAStoreTypeWStr property [Security], CAStoreTypeWStr property [Security],IEnroll interface, IEnroll interface [Security],CAStoreTypeWStr property, IEnroll.CAStoreTypeWStr, IEnroll.put_CAStoreTypeWStr, IEnroll::CAStoreTypeWStr, IEnroll::get_CAStoreTypeWStr, IEnroll::put_CAStoreTypeWStr, put_CAStoreTypeWStr, security.ienroll4_castoretypewstr, sz_CERT_STORE_PROV_SYSTEM_W, xenroll/IEnroll::CAStoreTypeWStr, xenroll/IEnroll::get_CAStoreTypeWStr, xenroll/IEnroll::put_CAStoreTypeWStr
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
 - IEnroll::put_CAStoreTypeWStr
 - xenroll/IEnroll::put_CAStoreTypeWStr
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
 - IEnroll.CAStoreTypeWStr
 - IEnroll.get_CAStoreTypeWStr
 - IEnroll.put_CAStoreTypeWStr
---

# IEnroll::put_CAStoreTypeWStr


## -description

<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>CAStoreTypeWStr</b> property sets or retrieves the type of store to use for the store specified by the 
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_castorenamewstr">CAStoreNameWStr</a> property. This store type is passed directly on to the  <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certopenstore">CertOpenStore</a> function.

The default value for this property is  sz_CERT_STORE_PROV_SYSTEM. Only system stores are supported. This property was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll">IEnroll</a> interface.

This property is read/write.

## -parameters

## -remarks

The <b>CAStoreTypeWStr</b> property affects the behavior of the following methods:

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

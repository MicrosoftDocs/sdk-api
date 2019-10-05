---
UID: NF:xenroll.IEnroll.put_MyStoreTypeWStr
title: IEnroll::put_MyStoreTypeWStr (xenroll.h)
author: windows-sdk-content
description: Sets or retrieves the type of store specified by the MyStoreTypeWStr property.
old-location: security\ienroll4_mystoretypewstr.htm
tech.root: SecCrypto
ms.assetid: 46f95ae3-efd2-4545-b31d-df04112aa737
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnroll interface [Security],MyStoreTypeWStr property, IEnroll.MyStoreTypeWStr, IEnroll.put_MyStoreTypeWStr, IEnroll::MyStoreTypeWStr, IEnroll::get_MyStoreTypeWStr, IEnroll::put_MyStoreTypeWStr, MyStoreTypeWStr property [Security], MyStoreTypeWStr property [Security],IEnroll interface, put_MyStoreTypeWStr, security.ienroll4_mystoretypewstr, sz_CERT_STORE_PROV_SYSTEM_W, xenroll/IEnroll::MyStoreTypeWStr, xenroll/IEnroll::get_MyStoreTypeWStr, xenroll/IEnroll::put_MyStoreTypeWStr
ms.topic: method
f1_keywords: 
 - "xenroll/IEnroll.MyStoreTypeWStr"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - IEnroll.MyStoreTypeWStr
 - IEnroll.get_MyStoreTypeWStr
 - IEnroll.put_MyStoreTypeWStr
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnroll::put_MyStoreTypeWStr


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>MyStoreTypeWStr</b> property sets or retrieves the type of store  specified by the 
<b>MyStoreTypeWStr</b> property.   This store type is passed directly on to <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certopenstore">CertOpenStore</a>.

The default value for this property is sz_CERT_STORE_PROV_SYSTEM. Only system stores are supported. This property was first defined in the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-ienroll">IEnroll</a> interface.

This property is read/write.


## -parameters


## -remarks




The <b>MyStoreTypeWStr</b> property affects the behavior of the following methods:

<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-acceptpkcs7blob">acceptPKCS7Blob</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-acceptfilepkcs7wstr">acceptFilePKCS7WStr</a>
</li>
</ul>





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll</a>
 

 


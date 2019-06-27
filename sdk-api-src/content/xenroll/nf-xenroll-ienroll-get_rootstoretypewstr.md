---
UID: NF:xenroll.IEnroll.get_RootStoreTypeWStr
title: IEnroll::get_RootStoreTypeWStr (xenroll.h)
author: windows-sdk-content
description: Sets or retrieves the type of store to use for the store specified by the RootStoreNameWStr property.
old-location: security\ienroll4_rootstoretypewstr.htm
tech.root: SecCrypto
ms.assetid: 42e50e99-a5ef-40b7-b6ef-c86272d1cd0d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnroll interface [Security],RootStoreTypeWStr property, IEnroll.RootStoreTypeWStr, IEnroll.get_RootStoreTypeWStr, IEnroll::RootStoreTypeWStr, IEnroll::get_RootStoreTypeWStr, IEnroll::put_RootStoreTypeWStr, RootStoreTypeWStr property [Security], RootStoreTypeWStr property [Security],IEnroll interface, get_RootStoreTypeWStr, security.ienroll4_rootstoretypewstr, sz_CERT_STORE_PROV_SYSTEM_W, xenroll/IEnroll::RootStoreTypeWStr, xenroll/IEnroll::get_RootStoreTypeWStr, xenroll/IEnroll::put_RootStoreTypeWStr
ms.topic: method
f1_keywords: 
 - "xenroll/IEnroll.RootStoreTypeWStr"
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
 - IEnroll.RootStoreTypeWStr
 - IEnroll.get_RootStoreTypeWStr
 - IEnroll.put_RootStoreTypeWStr
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnroll::get_RootStoreTypeWStr


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>RootStoreTypeWStr</b> property sets or retrieves the type of store to use for the store specified by the 
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_rootstorenamewstr">RootStoreNameWStr</a> property. This store type is passed directly on to the <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certopenstore">CertOpenStore</a> function.

The default value for this property is sz_CERT_STORE_PROV_SYSTEM. Only system stores are supported. This property was first defined in the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-ienroll">IEnroll</a> interface.

This property is read/write.


## -parameters


## -remarks




<b>RootStoreTypeWStr</b> affects the behavior of the following methods:

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
 

 


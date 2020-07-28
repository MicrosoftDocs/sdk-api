---
UID: NF:xenroll.IEnroll.get_MyStoreFlags
title: IEnroll::get_MyStoreFlags (xenroll.h)
description: Sets or retrieves the registry location used for the MY store.
helpviewer_keywords: ["IEnroll interface [Security]","MyStoreFlags property","IEnroll.MyStoreFlags","IEnroll.get_MyStoreFlags","IEnroll::MyStoreFlags","IEnroll::get_MyStoreFlags","IEnroll::put_MyStoreFlags","MyStoreFlags property [Security]","MyStoreFlags property [Security]","IEnroll interface","get_MyStoreFlags","security.ienroll4_mystoreflags","xenroll/IEnroll::MyStoreFlags","xenroll/IEnroll::get_MyStoreFlags","xenroll/IEnroll::put_MyStoreFlags"]
old-location: security\ienroll4_mystoreflags.htm
tech.root: security
ms.assetid: e545920a-0c39-49bb-90cc-87039d2e2cfd
ms.date: 12/05/2018
ms.keywords: IEnroll interface [Security],MyStoreFlags property, IEnroll.MyStoreFlags, IEnroll.get_MyStoreFlags, IEnroll::MyStoreFlags, IEnroll::get_MyStoreFlags, IEnroll::put_MyStoreFlags, MyStoreFlags property [Security], MyStoreFlags property [Security],IEnroll interface, get_MyStoreFlags, security.ienroll4_mystoreflags, xenroll/IEnroll::MyStoreFlags, xenroll/IEnroll::get_MyStoreFlags, xenroll/IEnroll::put_MyStoreFlags
f1_keywords:
- xenroll/IEnroll.MyStoreFlags
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
- IEnroll.MyStoreFlags
- IEnroll.get_MyStoreFlags
- IEnroll.put_MyStoreFlags
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnroll::get_MyStoreFlags


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>MyStoreFlags</b> property sets or retrieves the registry location used for the MY store.

The default value for  this property  is CERT_SYSTEM_STORE_CURRENT_USER. This property was first defined in the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-ienroll">IEnroll</a> interface.

This property is read/write.


## -parameters


## -remarks



The <b>MyStoreFlags</b> property value is passed to the 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certopenstore">CertOpenStore</a> CryptoAPI function by using its <i>dwFlags</i> parameter.


The <b>MyStoreFlags</b> property should be set before using the following methods:

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
 

 


---
UID: NF:xenroll.IEnroll.get_RootStoreFlags
title: IEnroll::get_RootStoreFlags (xenroll.h)
description: Sets or retrieves the registry location used for the root store. (Get)
helpviewer_keywords: ["IEnroll interface [Security]","RootStoreFlags property","IEnroll.RootStoreFlags","IEnroll.get_RootStoreFlags","IEnroll::RootStoreFlags","IEnroll::get_RootStoreFlags","IEnroll::put_RootStoreFlags","RootStoreFlags property [Security]","RootStoreFlags property [Security]","IEnroll interface","get_RootStoreFlags","security.ienroll4_rootstoreflags","xenroll/IEnroll::RootStoreFlags","xenroll/IEnroll::get_RootStoreFlags","xenroll/IEnroll::put_RootStoreFlags"]
old-location: security\ienroll4_rootstoreflags.htm
tech.root: security
ms.assetid: fa4640db-f3e5-4fe0-a696-26b5e13b7dd1
ms.date: 12/05/2018
ms.keywords: IEnroll interface [Security],RootStoreFlags property, IEnroll.RootStoreFlags, IEnroll.get_RootStoreFlags, IEnroll::RootStoreFlags, IEnroll::get_RootStoreFlags, IEnroll::put_RootStoreFlags, RootStoreFlags property [Security], RootStoreFlags property [Security],IEnroll interface, get_RootStoreFlags, security.ienroll4_rootstoreflags, xenroll/IEnroll::RootStoreFlags, xenroll/IEnroll::get_RootStoreFlags, xenroll/IEnroll::put_RootStoreFlags
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
 - IEnroll::get_RootStoreFlags
 - xenroll/IEnroll::get_RootStoreFlags
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
 - IEnroll.RootStoreFlags
 - IEnroll.get_RootStoreFlags
 - IEnroll.put_RootStoreFlags
---

# IEnroll::get_RootStoreFlags


## -description

<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>RootStoreFlags</b> property sets or retrieves the registry location used for the root store.

The default value for  this property  is CERT_SYSTEM_STORE_CURRENT_USER. This property was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll">IEnroll</a> interface.

This property is read/write.

## -parameters

## -remarks

The <b>RootStoreFlags</b> property value is passed to the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certopenstore">CertOpenStore</a> CryptoAPI function by using  its <i>dwFlags</i> parameter.


The <b>RootStoreFlags</b> property should be set before using the following methods:

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

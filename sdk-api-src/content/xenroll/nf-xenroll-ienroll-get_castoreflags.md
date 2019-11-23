---
UID: NF:xenroll.IEnroll.get_CAStoreFlags
title: IEnroll::get_CAStoreFlags (xenroll.h)

description: The CAStoreFlags property of IEnroll4 sets or retrieves a flag that controls the certification authority (CA) store when the store is opened.
old-location: security\ienroll4_castoreflags.htm
tech.root: SecCrypto
ms.assetid: 294a8a38-9c76-4e5c-ac11-2fcb8b81727e

ms.date: 12/05/2018
ms.keywords: CAStoreFlags property [Security], CAStoreFlags property [Security],IEnroll interface, IEnroll interface [Security],CAStoreFlags property, IEnroll.CAStoreFlags, IEnroll.get_CAStoreFlags, IEnroll::CAStoreFlags, IEnroll::get_CAStoreFlags, IEnroll::put_CAStoreFlags, get_CAStoreFlags, security.ienroll4_castoreflags, xenroll/IEnroll::CAStoreFlags, xenroll/IEnroll::get_CAStoreFlags, xenroll/IEnroll::put_CAStoreFlags
ms.topic: method
f1_keywords: 
 - "xenroll/IEnroll.CAStoreFlags"
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
 - IEnroll.CAStoreFlags
 - IEnroll.get_CAStoreFlags
 - IEnroll.put_CAStoreFlags
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnroll::get_CAStoreFlags


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>CAStoreFlags</b> property sets or retrieves a flag that controls the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) store when the store is opened. This flag is  passed to the <i>dwFlags</i> parameter of the <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certopenstore">CertOpenStore</a> function when the CA store is opened.

The default value for this property is CERT_SYSTEM_STORE_CURRENT_USER.  This property was first defined in the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-ienroll">IEnroll</a> interface.

This property is read/write.


## -parameters


## -remarks




The <b>CAStoreFlags</b> property affects the behavior of the following methods:

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
 

 


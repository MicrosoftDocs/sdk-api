---
UID: NF:wincrypt.CertRemoveStoreFromCollection
title: CertRemoveStoreFromCollection function (wincrypt.h)
description: Removes a sibling certificate store from a collection store.
helpviewer_keywords: ["CertRemoveStoreFromCollection","CertRemoveStoreFromCollection function [Security]","_crypto2_certremovestorefromcollection","security.certremovestorefromcollection","wincrypt/CertRemoveStoreFromCollection"]
old-location: security\certremovestorefromcollection.htm
tech.root: security
ms.assetid: e1564848-8b39-4ea9-9148-142ceaaaed15
ms.date: 12/05/2018
ms.keywords: CertRemoveStoreFromCollection, CertRemoveStoreFromCollection function [Security], _crypto2_certremovestorefromcollection, security.certremovestorefromcollection, wincrypt/CertRemoveStoreFromCollection
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CertRemoveStoreFromCollection
 - wincrypt/CertRemoveStoreFromCollection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertRemoveStoreFromCollection
---

# CertRemoveStoreFromCollection function


## -description

The <b>CertRemoveStoreFromCollection</b> function removes a sibling <a href="/windows/desktop/SecGloss/c-gly">certificate store</a> from a collection store.

## -parameters

### -param hCollectionStore [in]

A handle of the collection certificate store.

### -param hSiblingStore [in]

Handle of the sibling certificate store to be removed from the collection store.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddstoretocollection">CertAddStoreToCollection</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certopenstore">CertOpenStore</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate Store Functions</a>
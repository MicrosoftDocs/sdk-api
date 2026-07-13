---
UID: NN:objidl.IRootStorage
title: IRootStorage (objidl.h)
description: The IRootStorage interface contains a single method that switches a storage object to a different underlying file and saves the storage object to that file.
helpviewer_keywords: ["IRootStorage","IRootStorage interface [Structured Storage]","IRootStorage interface [Structured Storage]","described","_stg_irootstorage","objidl/IRootStorage","stg.irootstorage"]
old-location: stg\irootstorage.htm
tech.root: Stg
ms.assetid: cf92c62f-ef65-46b1-8f41-f2b31ff52044
ms.date: 12/05/2018
ms.keywords: IRootStorage, IRootStorage interface [Structured Storage], IRootStorage interface [Structured Storage],described, _stg_irootstorage, objidl/IRootStorage, stg.irootstorage
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRootStorage
 - objidl/IRootStorage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - IRootStorage
---

# IRootStorage interface


## -description

The 
<b>IRootStorage</b> interface contains a single method that switches a storage object to a different underlying file and saves the storage object to that file. The save operation occurs even with low-memory conditions and uncommitted changes to the storage object. A subsequent call to 
<a href="/windows/desktop/api/objidl/nf-objidl-istorage-commit">IStorage::Commit</a> is guaranteed to not consume additional memory.

## -inheritance

The <b>IRootStorage</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRootStorage</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a>



<a href="/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile">StgCreateDocfile</a>

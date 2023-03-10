---
UID: NN:objidl.IDirectWriterLock
title: IDirectWriterLock (objidl.h)
description: The IDirectWriterLock interface enables a single writer to obtain exclusive write access to a root storage object opened in direct mode while allowing concurrent access by multiple readers.
helpviewer_keywords: ["IDirectWriterLock","IDirectWriterLock interface [Structured Storage]","IDirectWriterLock interface [Structured Storage]","described","_stg_idirectwriterlock","objidl/IDirectWriterLock","stg.idirectwriterlock"]
old-location: stg\idirectwriterlock.htm
tech.root: Stg
ms.assetid: cff56e4f-b8c5-4d87-9289-f8f2212d7c42
ms.date: 12/05/2018
ms.keywords: IDirectWriterLock, IDirectWriterLock interface [Structured Storage], IDirectWriterLock interface [Structured Storage],described, _stg_idirectwriterlock, objidl/IDirectWriterLock, stg.idirectwriterlock
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
 - IDirectWriterLock
 - objidl/IDirectWriterLock
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
 - IDirectWriterLock
---

# IDirectWriterLock interface


## -description

The 
<b>IDirectWriterLock</b> interface enables a single writer to obtain exclusive write access to a root storage object opened in direct mode while allowing concurrent access by multiple readers. This single-writer, multiple-reader mode does not require the overhead of making a snapshot copy of the storage for the readers.

## -inheritance

The <b>IDirectWriterLock</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirectWriterLock</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a>



<a href="/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile">StgCreateDocfile</a>

---
UID: NN:strmif.IAMDevMemoryControl
title: IAMDevMemoryControl (strmif.h)
description: Note  This interface is no longer supported by the AVI Splitter. Note  It was defined to support certain older hardware decoders that required AVI files to be read directly into hardware memory.
helpviewer_keywords: ["IAMDevMemoryControl","IAMDevMemoryControl interface [DirectShow]","IAMDevMemoryControl interface [DirectShow]","described","IAMDevMemoryControlInterface","dshow.iamdevmemorycontrol","strmif/IAMDevMemoryControl"]
old-location: dshow\iamdevmemorycontrol.htm
tech.root: dshow
ms.assetid: 9945bffb-6748-4c7d-ba14-91470cf6c651
ms.date: 12/05/2018
ms.keywords: IAMDevMemoryControl, IAMDevMemoryControl interface [DirectShow], IAMDevMemoryControl interface [DirectShow],described, IAMDevMemoryControlInterface, dshow.iamdevmemorycontrol, strmif/IAMDevMemoryControl
req.header: strmif.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMDevMemoryControl
 - strmif/IAMDevMemoryControl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmif.h
api_name:
 - IAMDevMemoryControl
---

# IAMDevMemoryControl interface


## -description

<div class="alert"><b>Note</b>  This interface is no longer supported by the AVI Splitter.</div>
<div> </div>
<div class="alert"><b>Note</b>  It was defined to support certain older hardware decoders that required AVI files to be read directly into hardware memory. The interface enables the AVI parser to allocate memory from the downstream filter but still provide its own allocator. There should be no need for any newer devices to support this interface.</div>
<div> </div>
A device memory control object supports <code>IAMDevMemoryControl</code>. This object is aggregated with an <a href="/windows/desktop/api/strmif/nn-strmif-imemallocator">IMemAllocator</a> object that is used in the connection. Typically, filters will call the <a href="/windows/desktop/api/strmif/nf-strmif-iamdevmemoryallocator-getdevmemoryobject">IAMDevMemoryAllocator::GetDevMemoryObject</a> method to obtain a pointer to this interface.

Implement this interface with the <a href="/windows/desktop/api/strmif/nn-strmif-iamdevmemoryallocator">IAMDevMemoryAllocator</a> interface when pins need to have greater control of memory allocation.

Use this interface to synchronize the completion of writing data to a memory allocator, and to get the device ID of the on-board memory allocator.

## -inheritance

The <b>IAMDevMemoryControl</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMDevMemoryControl</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/deprecated-interfaces">Deprecated Interfaces</a>

---
UID: NF:amstream.IAMMediaTypeStream.GetStreamAllocatorRequirements
title: IAMMediaTypeStream::GetStreamAllocatorRequirements (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The GetStreamAllocatorRequirements retrieves the allocator requirements for the stream. This method is not currently implemented.
helpviewer_keywords: ["GetStreamAllocatorRequirements","GetStreamAllocatorRequirements method [DirectShow]","GetStreamAllocatorRequirements method [DirectShow]","IAMMediaTypeStream interface","IAMMediaTypeStream interface [DirectShow]","GetStreamAllocatorRequirements method","IAMMediaTypeStream.GetStreamAllocatorRequirements","IAMMediaTypeStream::GetStreamAllocatorRequirements","IAMMediaTypeStreamGetStreamAllocatorRequirements","amstream/IAMMediaTypeStream::GetStreamAllocatorRequirements","dshow.iammediatypestream_getstreamallocatorrequirements"]
old-location: dshow\iammediatypestream_getstreamallocatorrequirements.htm
tech.root: dshow
ms.assetid: 0a1ad5c5-0cbf-44a5-833f-951c9934bd19
ms.date: 12/05/2018
ms.keywords: GetStreamAllocatorRequirements, GetStreamAllocatorRequirements method [DirectShow], GetStreamAllocatorRequirements method [DirectShow],IAMMediaTypeStream interface, IAMMediaTypeStream interface [DirectShow],GetStreamAllocatorRequirements method, IAMMediaTypeStream.GetStreamAllocatorRequirements, IAMMediaTypeStream::GetStreamAllocatorRequirements, IAMMediaTypeStreamGetStreamAllocatorRequirements, amstream/IAMMediaTypeStream::GetStreamAllocatorRequirements, dshow.iammediatypestream_getstreamallocatorrequirements
req.header: amstream.h
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
 - IAMMediaTypeStream::GetStreamAllocatorRequirements
 - amstream/IAMMediaTypeStream::GetStreamAllocatorRequirements
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - amstream.h
api_name:
 - IAMMediaTypeStream.GetStreamAllocatorRequirements
---

# IAMMediaTypeStream::GetStreamAllocatorRequirements


## -description

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>GetStreamAllocatorRequirements</code> retrieves the allocator requirements for the stream. This method is not currently implemented.

## -parameters

### -param pProps [out]

Pointer to an <a href="/windows/win32/api/strmif/ns-strmif-allocator_properties">ALLOCATOR_PROPERTIES</a> structure that receives the stream allocator requirements.

## -returns

Returns E_FAIL.

## -see-also

<a href="/windows/desktop/api/amstream/nn-amstream-iammediatypestream">IAMMediaTypeStream Interface</a>
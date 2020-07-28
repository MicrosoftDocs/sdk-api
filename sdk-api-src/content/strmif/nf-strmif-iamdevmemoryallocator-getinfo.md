---
UID: NF:strmif.IAMDevMemoryAllocator.GetInfo
title: IAMDevMemoryAllocator::GetInfo (strmif.h)
description: Note  The IAMDevMemoryAllocator interface is deprecated. Retrieves information about the memory capabilities.
helpviewer_keywords: ["GetInfo","GetInfo method [DirectShow]","GetInfo method [DirectShow]","IAMDevMemoryAllocator interface","IAMDevMemoryAllocator interface [DirectShow]","GetInfo method","IAMDevMemoryAllocator.GetInfo","IAMDevMemoryAllocator::GetInfo","IAMDevMemoryAllocatorGetInfo","dshow.iamdevmemoryallocator_getinfo","strmif/IAMDevMemoryAllocator::GetInfo"]
old-location: dshow\iamdevmemoryallocator_getinfo.htm
tech.root: dshow
ms.assetid: ee3070ed-98df-4f20-a91f-bb3c3492f3d8
ms.date: 12/05/2018
ms.keywords: GetInfo, GetInfo method [DirectShow], GetInfo method [DirectShow],IAMDevMemoryAllocator interface, IAMDevMemoryAllocator interface [DirectShow],GetInfo method, IAMDevMemoryAllocator.GetInfo, IAMDevMemoryAllocator::GetInfo, IAMDevMemoryAllocatorGetInfo, dshow.iamdevmemoryallocator_getinfo, strmif/IAMDevMemoryAllocator::GetInfo
f1_keywords:
- strmif/IAMDevMemoryAllocator.GetInfo
dev_langs:
- c++
req.header: strmif.h
req.include-header: Dshow.h
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmif.h
api_name:
- IAMDevMemoryAllocator.GetInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMDevMemoryAllocator::GetInfo


## -description



<div class="alert"><b>Note</b>  The <b>IAMDevMemoryAllocator</b> interface is deprecated.</div>
<div> </div>
Retrieves information about the memory capabilities.




## -parameters




### -param pdwcbTotalFree [out]

Pointer to the total free memory size.


### -param pdwcbLargestFree [out]

Pointer to the returned largest free memory size.


### -param pdwcbTotalMemory [out]

Pointer to the returned total memory size.


### -param pdwcbMinimumChunk [out]

Pointer to the returned minimum chunk size, giving granularity and alignment rules.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



Use this method to find out the total amount of memory available. This method returns values for the entire on-board memory that is available on that device. If multiple filters (devices) share the memory, it will return the amount available to that specific device, which might be a portion of the total amount of on-board memory. This amount will be implementation-specific. For example, the on-board memory manager on the codec might be able to access all 32 megabytes (MB) of memory on the card. However, individual pin implementations of <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamdevmemoryallocator">IAMDevMemoryAllocator</a> only report a portion of this memory.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamdevmemoryallocator">IAMDevMemoryAllocator Interface</a>
 

 


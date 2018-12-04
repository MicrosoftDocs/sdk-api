---
UID: NF:strmif.IAMDevMemoryAllocator.GetDevMemoryObject
title: IAMDevMemoryAllocator::GetDevMemoryObject
author: windows-sdk-content
description: Note  The IAMDevMemoryAllocator interface is deprecated. Retrieves an IUnknown interface pointer to a device memory control object that can be aggregated with a custom allocator.
old-location: dshow\iamdevmemoryallocator_getdevmemoryobject.htm
tech.root: DirectShow
ms.assetid: d7ca361a-1ce6-449f-9d81-fbfe39f0f9f0
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetDevMemoryObject, GetDevMemoryObject method [DirectShow], GetDevMemoryObject method [DirectShow],IAMDevMemoryAllocator interface, IAMDevMemoryAllocator interface [DirectShow],GetDevMemoryObject method, IAMDevMemoryAllocator.GetDevMemoryObject, IAMDevMemoryAllocator::GetDevMemoryObject, IAMDevMemoryAllocatorGetDevMemoryObject, dshow.iamdevmemoryallocator_getdevmemoryobject, strmif/IAMDevMemoryAllocator::GetDevMemoryObject
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IAMDevMemoryAllocator.GetDevMemoryObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMDevMemoryAllocator::GetDevMemoryObject


## -description



<div class="alert"><b>Note</b>  The <b>IAMDevMemoryAllocator</b> interface is deprecated.</div>
<div> </div>
Retrieves an <b>IUnknown</b> interface pointer to a device memory control object that can be aggregated with a custom allocator.




## -parameters




### -param ppUnkInnner [out]

Address of a pointer to the newly created control object's own <b>IUnknown</b>. This inner <b>IUnknown</b> interface should be released when the outer object is destroyed. The custom allocator should call the <b>QueryInterface</b> method on this pointer to obtain the <a href="https://msdn.microsoft.com/9945bffb-6748-4c7d-ba14-91470cf6c651">IAMDevMemoryControl</a> interface.


### -param pUnkOuter [in]

Pointer to the custom allocator's own <b>IUnknown</b> interface. This interface aggregates the device memory control object inside the custom allocator.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



The device memory control object is necessary to aggregate with the custom allocator, because renderers that require the use of on-board memory will query for <a href="https://msdn.microsoft.com/9945bffb-6748-4c7d-ba14-91470cf6c651">IAMDevMemoryControl</a> when they receive a new allocator, to verify that the memory is from the same device. This occurs because the hardware filter will receive an <a href="https://msdn.microsoft.com/77a161c4-706c-4270-a343-9e16c03cd590">IMemAllocator</a> object, which might or might not use the on-board memory. To decide if it is a compatible allocator, the object would query for the <b>IAMDevMemoryControl</b> interface to access specific methods. The <b>IAMDevMemoryControl</b> creates an aggregated object that implements the methods of <b>IAMDevMemoryControl</b> (these are often hardware-specific).

See COM documentation for rules on how the outer object implements aggregation.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/bab1e582-928a-408b-a9c5-8e9827e9928b">IAMDevMemoryAllocator Interface</a>
 

 


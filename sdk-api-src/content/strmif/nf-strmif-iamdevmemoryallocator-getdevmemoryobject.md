---
UID: NF:strmif.IAMDevMemoryAllocator.GetDevMemoryObject
title: IAMDevMemoryAllocator::GetDevMemoryObject (strmif.h)
description: Note  The IAMDevMemoryAllocator interface is deprecated. Retrieves an IUnknown interface pointer to a device memory control object that can be aggregated with a custom allocator.
helpviewer_keywords: ["GetDevMemoryObject","GetDevMemoryObject method [DirectShow]","GetDevMemoryObject method [DirectShow]","IAMDevMemoryAllocator interface","IAMDevMemoryAllocator interface [DirectShow]","GetDevMemoryObject method","IAMDevMemoryAllocator.GetDevMemoryObject","IAMDevMemoryAllocator::GetDevMemoryObject","IAMDevMemoryAllocatorGetDevMemoryObject","dshow.iamdevmemoryallocator_getdevmemoryobject","strmif/IAMDevMemoryAllocator::GetDevMemoryObject"]
old-location: dshow\iamdevmemoryallocator_getdevmemoryobject.htm
tech.root: dshow
ms.assetid: d7ca361a-1ce6-449f-9d81-fbfe39f0f9f0
ms.date: 12/05/2018
ms.keywords: GetDevMemoryObject, GetDevMemoryObject method [DirectShow], GetDevMemoryObject method [DirectShow],IAMDevMemoryAllocator interface, IAMDevMemoryAllocator interface [DirectShow],GetDevMemoryObject method, IAMDevMemoryAllocator.GetDevMemoryObject, IAMDevMemoryAllocator::GetDevMemoryObject, IAMDevMemoryAllocatorGetDevMemoryObject, dshow.iamdevmemoryallocator_getdevmemoryobject, strmif/IAMDevMemoryAllocator::GetDevMemoryObject
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMDevMemoryAllocator::GetDevMemoryObject
 - strmif/IAMDevMemoryAllocator::GetDevMemoryObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IAMDevMemoryAllocator.GetDevMemoryObject
---

# IAMDevMemoryAllocator::GetDevMemoryObject


## -description

<div class="alert"><b>Note</b>  The <b>IAMDevMemoryAllocator</b> interface is deprecated.</div>
<div> </div>
Retrieves an <b>IUnknown</b> interface pointer to a device memory control object that can be aggregated with a custom allocator.

## -parameters

### -param ppUnkInnner [out]

Address of a pointer to the newly created control object's own <b>IUnknown</b>. This inner <b>IUnknown</b> interface should be released when the outer object is destroyed. The custom allocator should call the <b>QueryInterface</b> method on this pointer to obtain the <a href="/windows/desktop/api/strmif/nn-strmif-iamdevmemorycontrol">IAMDevMemoryControl</a> interface.

### -param pUnkOuter [in]

Pointer to the custom allocator's own <b>IUnknown</b> interface. This interface aggregates the device memory control object inside the custom allocator.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

The device memory control object is necessary to aggregate with the custom allocator, because renderers that require the use of on-board memory will query for <a href="/windows/desktop/api/strmif/nn-strmif-iamdevmemorycontrol">IAMDevMemoryControl</a> when they receive a new allocator, to verify that the memory is from the same device. This occurs because the hardware filter will receive an <a href="/windows/desktop/api/strmif/nn-strmif-imemallocator">IMemAllocator</a> object, which might or might not use the on-board memory. To decide if it is a compatible allocator, the object would query for the <b>IAMDevMemoryControl</b> interface to access specific methods. The <b>IAMDevMemoryControl</b> creates an aggregated object that implements the methods of <b>IAMDevMemoryControl</b> (these are often hardware-specific).

See COM documentation for rules on how the outer object implements aggregation.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamdevmemoryallocator">IAMDevMemoryAllocator Interface</a>
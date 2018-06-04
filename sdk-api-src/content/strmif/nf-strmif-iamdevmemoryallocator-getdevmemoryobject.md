---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IAMDevMemoryAllocator::GetDevMemoryObject


## -description



<div class="alert"><b>Note</b>  The <b>IAMDevMemoryAllocator</b> interface is deprecated.</div>
<div> </div>
Retrieves an <b>IUnknown</b> interface pointer to a device memory control object that can be aggregated with a custom allocator.




## -parameters




### -param ppUnkInnner




### -param pUnkOuter [in]

Pointer to the custom allocator's own <b>IUnknown</b> interface. This interface aggregates the device memory control object inside the custom allocator.


#### - ppUnkInner [out]

Address of a pointer to the newly created control object's own <b>IUnknown</b>. This inner <b>IUnknown</b> interface should be released when the outer object is destroyed. The custom allocator should call the <b>QueryInterface</b> method on this pointer to obtain the <a href="https://msdn.microsoft.com/9945bffb-6748-4c7d-ba14-91470cf6c651">IAMDevMemoryControl</a> interface.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



The device memory control object is necessary to aggregate with the custom allocator, because renderers that require the use of on-board memory will query for <a href="https://msdn.microsoft.com/9945bffb-6748-4c7d-ba14-91470cf6c651">IAMDevMemoryControl</a> when they receive a new allocator, to verify that the memory is from the same device. This occurs because the hardware filter will receive an <a href="https://msdn.microsoft.com/77a161c4-706c-4270-a343-9e16c03cd590">IMemAllocator</a> object, which might or might not use the on-board memory. To decide if it is a compatible allocator, the object would query for the <b>IAMDevMemoryControl</b> interface to access specific methods. The <b>IAMDevMemoryControl</b> creates an aggregated object that implements the methods of <b>IAMDevMemoryControl</b> (these are often hardware-specific).

See COM documentation for rules on how the outer object implements aggregation.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/bab1e582-928a-408b-a9c5-8e9827e9928b">IAMDevMemoryAllocator Interface</a>
 

 


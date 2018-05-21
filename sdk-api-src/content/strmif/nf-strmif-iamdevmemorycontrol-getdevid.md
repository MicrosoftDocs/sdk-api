---
UID: NF:strmif.IAMDevMemoryControl.GetDevId
title: IAMDevMemoryControl::GetDevId
author: windows-driver-content
description: Note  The IAMDevMemoryControl interface is deprecated. Retrieves the device ID of the on-board memory allocator.
old-location: dshow\iamdevmemorycontrol_getdevid.htm
old-project: DirectShow
ms.assetid: 398cc4b3-c025-4df4-8447-bd4599293dab
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: GetDevId, GetDevId method [DirectShow], GetDevId method [DirectShow],IAMDevMemoryControl interface, IAMDevMemoryControl interface [DirectShow],GetDevId method, IAMDevMemoryControl.GetDevId, IAMDevMemoryControl::GetDevId, IAMDevMemoryControlGetDevId, dshow.iamdevmemorycontrol_getdevid, strmif/IAMDevMemoryControl::GetDevId
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmif.h
api_name:
-	IAMDevMemoryControl.GetDevId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMDevMemoryControl::GetDevId


## -description



<div class="alert"><b>Note</b>  The <b>IAMDevMemoryControl</b> interface is deprecated.</div>
<div> </div>
Retrieves the device ID of the on-board memory allocator.




## -parameters




### -param pdwDevId [out]

Pointer to the device ID.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -remarks



This method retrieves a unique ID that the hardware filter can use to verify that the specified allocator passed uses its on-board memory (because there can be more than one). The ID will be the same one as used to create the allocator object (using <b>CoCreateInstance</b>). For another filter to be able to use the on-board memory, it must have the same device ID as the on-board memory allocator.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/9945bffb-6748-4c7d-ba14-91470cf6c651">IAMDevMemoryControl Interface</a>
 

 


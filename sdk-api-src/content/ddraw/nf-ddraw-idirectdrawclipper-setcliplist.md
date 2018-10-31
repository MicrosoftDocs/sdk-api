---
UID: NF:ddraw.IDirectDrawClipper.SetClipList
title: IDirectDrawClipper::SetClipList
author: windows-sdk-content
description: Sets or deletes the clip list that is used by the IDirectDrawSurface7::Blt, IDirectDrawSurface7::BltBatch, and IDirectDrawSurface7::UpdateOverlay methods on surfaces to which the parent DirectDrawClipper object is attached.
old-location: directdraw\idirectdrawclipper_setcliplist.htm
tech.root: directdraw
ms.assetid: 717f51e0-80cb-4762-b05d-30e30d065d0c
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IDirectDrawClipper interface [DirectDraw],SetClipList method, IDirectDrawClipper.SetClipList, IDirectDrawClipper::SetClipList, SetClipList, SetClipList method [DirectDraw], SetClipList method [DirectDraw],IDirectDrawClipper interface, ddraw/IDirectDrawClipper::SetClipList, directdraw.idirectdrawclipper_setcliplist
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ddraw.h
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
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ddraw.dll
api_name:
 - IDirectDrawClipper.SetClipList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectDrawClipper::SetClipList


## -description


Sets or deletes the clip list that is used by the <a href="https://msdn.microsoft.com/e458c430-855c-419b-aa50-144d2b422e78">IDirectDrawSurface7::Blt</a>, <a href="https://msdn.microsoft.com/50c071a6-2963-474e-994e-c789b1924d92">IDirectDrawSurface7::BltBatch</a>, and <a href="https://msdn.microsoft.com/8706c6ca-cd17-490a-8ff9-9470a7d7a150">IDirectDrawSurface7::UpdateOverlay</a> methods on surfaces to which the parent DirectDrawClipper object is attached.


## -parameters




### -param arg1 [in]

A pointer to a valid <a href="https://msdn.microsoft.com/3eac0b23-3138-4b34-9c16-6cc185e4de22">RGNDATA</a> structure for the clip list to set or NULL. If there is an existing clip list that is associated with the DirectDrawClipper object and this value is NULL, the clip list is deleted.


### -param arg2 [in]

Currently not used and must be set to 0.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_CLIPPERISUSINGHWND</li>
<li>DDERR_INVALIDCLIPLIST</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_OUTOFMEMORY</li>
</ul>



## -remarks



You cannot set the clip list if a window handle is already associated with the DirectDrawClipper object. 

The <a href="https://msdn.microsoft.com/ac882b48-87b2-4b65-99b0-ac9065b5f47f">IDirectDrawSurface7::BltFast</a> method cannot clip. If you call <b>IDirectDrawSurface7::BltFast</b> on a surface with an attached clipper, it returns DDERR_UNSUPPORTED.

You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the  <b>SetClipList</b> method.




## -see-also




<a href="https://msdn.microsoft.com/2e93583a-59a8-4a0f-9299-ed57fdcebf33">IDirectDrawClipper</a>
 

 


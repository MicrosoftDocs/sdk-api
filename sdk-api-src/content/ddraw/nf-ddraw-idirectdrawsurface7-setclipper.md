---
UID: NF:ddraw.IDirectDrawSurface7.SetClipper
title: IDirectDrawSurface7::SetClipper
author: windows-sdk-content
description: Attaches a clipper object to, or deletes one from, this surface.
old-location: directdraw\idirectdrawsurface7_setclipper.htm
old-project: directdraw
ms.assetid: 18bc8018-b00c-40ef-a54a-e2eecdb835a9
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: IDirectDrawSurface7 interface [DirectDraw],SetClipper method, IDirectDrawSurface7.SetClipper, IDirectDrawSurface7::SetClipper, SetClipper, SetClipper method [DirectDraw], SetClipper method [DirectDraw],IDirectDrawSurface7 interface, ddraw/IDirectDrawSurface7::SetClipper, directdraw.idirectdrawsurface7_setclipper
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DEDUP_CONTAINER_EXTENT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ddraw.dll
api_name:
 - IDirectDrawSurface7.SetClipper
product: Windows
targetos: Windows
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
---

# IDirectDrawSurface7::SetClipper


## -description


Attaches a clipper object to, or deletes one from, this surface.


## -parameters






#### - lpDDClipper [in]

A pointer to the <a href="https://msdn.microsoft.com/2e93583a-59a8-4a0f-9299-ed57fdcebf33">IDirectDrawClipper</a> interface for the DirectDrawClipper object to be attached to the DirectDrawSurface object. If you set this parameter to NULL, the current DirectDrawClipper object is detached.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_INVALIDSURFACETYPE</li>
<li>DDERR_NOCLIPPERATTACHED</li>
</ul>



## -remarks



When you set a clipper to a surface for the first time, <b>SetClipper</b> increments the clipper's reference count; subsequent calls do not affect the clipper's reference count. If you pass NULL as the <i>lpDDClipper</i> parameter, the clipper is removed from the surface, and the clipper's reference count is decremented. If you do not delete the clipper, the surface automatically releases its reference to the clipper when the surface itself is released. According to COM rules, your application must release any references that it holds to the clipper when the object is no longer needed.

<b>SetClipper</b> is primarily used by surfaces that are being overlaid on or bitbltted to the primary surface. However, it can be used on any surface. After a DirectDrawClipper object has been attached and a clip list is associated with it, the DirectDrawClipper object is used for the <a href="https://msdn.microsoft.com/e458c430-855c-419b-aa50-144d2b422e78">IDirectDrawSurface7::Blt</a>, <a href="https://msdn.microsoft.com/50c071a6-2963-474e-994e-c789b1924d92">IDirectDrawSurface7::BltBatch</a>, and <a href="https://msdn.microsoft.com/8706c6ca-cd17-490a-8ff9-9470a7d7a150">IDirectDrawSurface7::UpdateOverlay</a> operations that involve the parent DirectDrawSurface object. <b>SetClipper</b> can also detach the current DirectDrawClipper object of a DirectDrawSurface object.



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the  <b>SetClipper</b> method.




## -see-also




<a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a>
 

 


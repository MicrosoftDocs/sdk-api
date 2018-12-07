---
UID: NF:ddraw.IDirectDrawSurface7.DeleteAttachedSurface
title: IDirectDrawSurface7::DeleteAttachedSurface
author: windows-sdk-content
description: Detaches one or more attached surfaces.
old-location: directdraw\idirectdrawsurface7_deleteattachedsurface.htm
tech.root: directdraw
ms.assetid: 39cefecd-2ae0-42ba-8140-842acdaa1ad8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DeleteAttachedSurface, DeleteAttachedSurface method [DirectDraw], DeleteAttachedSurface method [DirectDraw],IDirectDrawSurface7 interface, IDirectDrawSurface7 interface [DirectDraw],DeleteAttachedSurface method, IDirectDrawSurface7.DeleteAttachedSurface, IDirectDrawSurface7::DeleteAttachedSurface, ddraw/IDirectDrawSurface7::DeleteAttachedSurface, directdraw.idirectdrawsurface7_deleteattachedsurface
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
 - IDirectDrawSurface7.DeleteAttachedSurface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectDrawSurface7::DeleteAttachedSurface


## -description


Detaches one or more attached surfaces.


## -parameters




### -param arg1 [in]

Currently not used and must be set to 0.


### -param arg2 [in]

A pointer to the <a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a> interface for the DirectDrawSurface object to be detached. If this parameter is NULL, all attached surfaces become detached.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_CANNOTDETACHSURFACE</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_SURFACELOST</li>
<li>DDERR_SURFACENOTATTACHED</li>
</ul>



## -remarks



<b>DeleteAttachedSurface</b> decrements the reference count of the surface to be detached. If the reference count of the surface to be detached reaches 0, the surface is lost and removed from memory.

Implicit attachments, those formed by DirectDraw rather than the <a href="https://msdn.microsoft.com/6d42c5ed-7f05-4450-b1f4-cb9ee6efa7d9">IDirectDrawSurface7::AddAttachedSurface</a> method, cannot be detached. Detaching surfaces from a flipping chain can alter other surfaces in the chain. If a front buffer is detached from a flipping chain, the next surface in the chain becomes the front buffer, and the following surface becomes the back buffer. If a back buffer is detached from a chain, the following surface becomes a back buffer. If a plain surface is detached from a chain, the chain simply becomes shorter. If a flipping chain has only two surfaces and they are detached, the chain is destroyed, and both surfaces return to their previous designations.



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the <b>DeleteAttachedSurface</b> method.




## -see-also




<a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a>
 

 


---
UID: NF:ddraw.IDirectDrawSurface7.AddAttachedSurface
title: IDirectDrawSurface7::AddAttachedSurface
author: windows-sdk-content
description: Attaches the specified z-buffer surface to this surface.
old-location: directdraw\idirectdrawsurface7_addattachedsurface.htm
tech.root: directdraw
ms.assetid: 6d42c5ed-7f05-4450-b1f4-cb9ee6efa7d9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AddAttachedSurface, AddAttachedSurface method [DirectDraw], AddAttachedSurface method [DirectDraw],IDirectDrawSurface7 interface, IDirectDrawSurface7 interface [DirectDraw],AddAttachedSurface method, IDirectDrawSurface7.AddAttachedSurface, IDirectDrawSurface7::AddAttachedSurface, ddraw/IDirectDrawSurface7::AddAttachedSurface, directdraw.idirectdrawsurface7_addattachedsurface
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
 - IDirectDrawSurface7.AddAttachedSurface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectDrawSurface7::AddAttachedSurface


## -description


Attaches the specified z-buffer surface to this surface.



## -parameters






#### - lpDDSurface [in]

Address of the <a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a> interface for the surface to be attached.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_CANNOTATTACHSURFACE</li>
<li>DDERR_GENERIC</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_SURFACEALREADYATTACHED</li>
<li>DDERR_SURFACELOST</li>
<li>DDERR_WASSTILLDRAWING</li>
</ul>



## -remarks



<b>AddAttachedSurface</b> increments the reference count of the surface being attached. You can explicitly unattach the surface and decrement its reference count by using the <a href="https://msdn.microsoft.com/39cefecd-2ae0-42ba-8140-842acdaa1ad8">IDirectDrawSurface7::DeleteAttachedSurface</a> method. Unlike complex surfaces that you create with a single call to <a href="https://msdn.microsoft.com/4f27e36f-d04f-43ce-9a3d-64c352c8f8d8">IDirectDraw7::CreateSurface</a>, surfaces attached with this method are not automatically released. The application must release such surfaces.

You can attach only z-buffer surfaces with this method.

You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the <b>AddAttachedSurface</b> method.




## -see-also




<a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a>
 

 


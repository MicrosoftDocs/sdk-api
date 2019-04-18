---
UID: NF:ddraw.IDirectDraw7.FlipToGDISurface
title: IDirectDraw7::FlipToGDISurface (ddraw.h)
author: windows-sdk-content
description: Makes the surface that the GDI writes to the primary surface.
old-location: directdraw\idirectdraw7_fliptogdisurface.htm
tech.root: directdraw
ms.assetid: 495cace2-a315-4937-b0d9-9f77f5d95f66
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FlipToGDISurface, FlipToGDISurface method [DirectDraw], FlipToGDISurface method [DirectDraw],IDirectDraw7 interface, IDirectDraw7 interface [DirectDraw],FlipToGDISurface method, IDirectDraw7.FlipToGDISurface, IDirectDraw7::FlipToGDISurface, ddraw/IDirectDraw7::FlipToGDISurface, directdraw.idirectdraw7_fliptogdisurface
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
 - IDirectDraw7.FlipToGDISurface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectDraw7::FlipToGDISurface


## -description


Makes the surface that the GDI writes to the primary surface.


## -parameters






## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_NOTFOUND</li>
</ul>



## -remarks



You can call  <b>FlipToGDISurface</b> at the end of a page-flipping application to ensure that the display memory that the GDI writes to is visible.

You can also use  <b>FlipToGDISurface</b> to make the GDI surface the primary surface so that normal windows, such as dialog boxes, can be displayed in full-screen mode. The hardware must have the <a href="https://msdn.microsoft.com/en-us/library/Gg426101(v=VS.85).aspx">DDCAPS2_CANRENDERWINDOWED</a> capability.

<b>FlipToGDISurface</b> disables stereo autoflipping.

You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the  <b>FlipToGDISurface</b> method.




## -see-also




<a href="https://msdn.microsoft.com/1a1164fe-00c2-4469-8346-f86f7f48781e">IDirectDraw7</a>
 

 


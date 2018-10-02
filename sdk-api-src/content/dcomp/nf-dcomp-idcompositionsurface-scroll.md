---
UID: NF:dcomp.IDCompositionSurface.Scroll
title: IDCompositionSurface::Scroll
author: windows-sdk-content
description: Scrolls a rectangular area of a Microsoft DirectComposition logical surface.
old-location: directcomp\idcompositionsurface_scroll.htm
tech.root: directcomp
ms.assetid: 0764C59A-DDDE-420C-B044-827B7EDC6CF1
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IDCompositionSurface interface [DirectComposition],Scroll method, IDCompositionSurface.Scroll, IDCompositionSurface::Scroll, Scroll, Scroll method [DirectComposition], Scroll method [DirectComposition],IDCompositionSurface interface, dcomp/IDCompositionSurface::Scroll, directcomp.idcompositionsurface_scroll
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dcomp.lib
req.dll: Dcomp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionSurface.Scroll
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionSurface::Scroll


## -description


Scrolls a rectangular area of a Microsoft DirectComposition logical surface.


## -parameters




### -param scrollRect [in]

The rectangular area of the surface to be scrolled, relative to the upper-left corner of the surface. If this parameter is NULL, the entire surface is scrolled.


### -param clipRect [in, optional]

The <i>clipRect</i> clips the destination (<i>scrollRect</i> after offset) of the scroll.
The only bitmap content that will be scrolled are those that remain inside the clip rectangle after the scroll is completed.


### -param offsetX [in]

The amount of horizontal scrolling, in pixels. Use positive values to scroll right, and negative values to scroll left.


### -param offsetY [in]

The amount of vertical scrolling, in pixels. Use positive values to scroll down, and negative values to scroll up.


## -returns



If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method allows an application to blt/copy a sub-rectangle of a DirectComposition surface object. This avoids re-rendering content that is already available.  



The <i>scrollRect</i> rectangle must be contained in the boundaries of the surface.  If the <i>scrollRect</i> rectangle goes outside the bounds of the surface, this method fails.



The bits copied by the scroll operation (source) are defined by the intersection of the <i>scrollRect</i> and <i>clipRect</i> rectangles.  

The bits shown on the screen (destination) are defined by the intersection of the offset source rectangle and <i>clipRect</i>.



Scroll operations can only be called before calling <a href="https://msdn.microsoft.com/0D7E90A1-90E4-44BE-A4DA-8DA300C81A35">BeginDraw</a> or after calling <a href="https://msdn.microsoft.com/127195F7-6000-4D8C-B850-3E4D40BC4082">EndDraw</a>.  Suspended or resumed surfaces are not candidates for scrolling because they are still being updated.



The application is responsible for ensuring that the scrollable area for an <a href="https://msdn.microsoft.com/51E8D52C-2446-46B6-A5C1-0DC7FA9DF4CC">IDCompositionVirtualSurface</a> is limited to valid pixels. The behavior for invalid pixels in the <i>scrollRect</i> is undefined.  

Virtual surface sub-rectangular areas that were discarded by a trim or a resize operation can't be scrolled even if the trim or resize is applied in the same batch.  <a href="https://msdn.microsoft.com/5A4F516F-B031-47E6-9A3D-068CF2C3D53A">Trim</a> and <a href="https://msdn.microsoft.com/BB86CDA8-1DF0-436D-9FA3-95293E2B8C0E">Resize</a> are applied immediately.






## -see-also




<a href="https://msdn.microsoft.com/E271B4DC-5F09-426A-A5D3-43A48F30CB24">IDCompositionSurface</a>
 

 


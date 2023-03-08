---
UID: NF:ddraw.IDirectDraw7.GetAvailableVidMem
title: IDirectDraw7::GetAvailableVidMem (ddraw.h)
description: Retrieves the total amount of display memory available and the amount of display memory currently free for a given type of surface.
helpviewer_keywords: ["GetAvailableVidMem","GetAvailableVidMem method [DirectDraw]","GetAvailableVidMem method [DirectDraw]","IDirectDraw7 interface","IDirectDraw7 interface [DirectDraw]","GetAvailableVidMem method","IDirectDraw7.GetAvailableVidMem","IDirectDraw7::GetAvailableVidMem","ddraw/IDirectDraw7::GetAvailableVidMem","directdraw.idirectdraw7_getavailablevidmem"]
old-location: directdraw\idirectdraw7_getavailablevidmem.htm
tech.root: directdraw
ms.assetid: f7bfa81c-8e21-44ec-bed4-9b92aa099f00
ms.date: 12/05/2018
ms.keywords: GetAvailableVidMem, GetAvailableVidMem method [DirectDraw], GetAvailableVidMem method [DirectDraw],IDirectDraw7 interface, IDirectDraw7 interface [DirectDraw],GetAvailableVidMem method, IDirectDraw7.GetAvailableVidMem, IDirectDraw7::GetAvailableVidMem, ddraw/IDirectDraw7::GetAvailableVidMem, directdraw.idirectdraw7_getavailablevidmem
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectDraw7::GetAvailableVidMem
 - ddraw/IDirectDraw7::GetAvailableVidMem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ddraw.dll
api_name:
 - IDirectDraw7.GetAvailableVidMem
---

# IDirectDraw7::GetAvailableVidMem


## -description

Retrieves the total amount of display memory available and the amount of display memory currently free for a given type of surface.

## -parameters

### -param unnamedParam1 [in]

A pointer to a <a href="/previous-versions/windows/hardware/drivers/ff550292(v=vs.85)">DDSCAPS2</a> structure that indicates the hardware capabilities of the proposed surface.

### -param unnamedParam2 [out]

A pointer to a variable that receives the total amount of display memory available, in bytes. The value received reflects the total video memory, minus the video memory required for the primary surface and any private caches that the display driver reserves.

### -param unnamedParam3 [out]

A pointer to a variable that receives the amount of display memory currently free that can be allocated for a surface that matches the capabilities specified by the structure at <i>lpDDSCaps2</i>.

## -returns

If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDCAPS</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_NODIRECTDRAWHW</li>
</ul>

## -remarks

The following C++ example demonstrates how to use <b>GetAvailableVidMem</b> to determine both the total and free display memory available for texture-map surfaces:


```
// For this example, the lpDD variable is a valid 
// pointer to an IDirectDraw7 interface.
LPDIRECTDRAW7 lpDD;
DDSCAPS2      ddsCaps2; 
DWORD         dwTotal; 
DWORD         dwFree;
HRESULT       hr; 
 
hr = lpDD->QueryInterface(IID_IDirectDraw7, &lpDD); 
if (FAILED(hr))
    return hr; 
 
// Initialize the structure.
ZeroMemory(&ddsCaps2, sizeof(ddsCaps2));
 
ddsCaps2.dwCaps = DDSCAPS_TEXTURE; 
hr = lpDD->GetAvailableVidMem(&ddsCaps2, &dwTotal, &dwFree); 
if (FAILED(hr))
    return hr;


```


If the surface has the <a href="/previous-versions/windows/hardware/drivers/ff550286(v=vs.85)">DDSCAPS_VIDEOMEMORY</a> flag set, <b>GetAvailableVidMem</b> returns different amounts of video memory depending on whether the surface can be used as a 3-D texture. If the surface can be used for 3-D textures, <b>GetAvailableVidMem</b> returns the sum of the local video memory and the non-local video memory on AGP systems.

<b>GetAvailableVidMem</b> provides only a snapshot of the current display-memory state. The amount of free display memory is subject to change as surfaces are created and released. Therefore, you should use the free memory value only as an approximation. In addition, a particular display adapter card might make no distinction between two different memory types. For example, the adapter might use the same portion of display memory to store z-buffers and textures. So, allocating one type of surface (for example, a z-buffer) can affect the amount of display memory available for another type of surface (textures). Therefore, it is best to first allocate an application's fixed resources (such as front and back buffers and z-buffers) before determining how much memory is available for dynamic use (such as texture mapping).



<b>GetAvailableVidMem</b> was not implemented in the previous DirectX IDirectDraw interface version.





## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdraw7">IDirectDraw7</a>
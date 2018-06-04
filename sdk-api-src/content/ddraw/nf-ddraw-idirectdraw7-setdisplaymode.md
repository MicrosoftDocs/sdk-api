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

# IDirectDraw7::SetDisplayMode


## -description


Sets the mode of the display-device hardware.


## -parameters




### -param






#### - dwBPP [in]

Bits per pixel (bpp) of the new display mode.


#### - dwFlags [in]

This value consists of flags that describe additional options. Currently, the only valid flag is DDSDM_STANDARDVGAMODE, which causes the method to set Mode 13, instead of Mode X 320x200x8 mode. If you are setting another resolution, bit depth, or a Mode X mode, do not use this flag; instead, set the parameter to 0.


#### - dwHeight [in]

Height of the new display mode.


#### - dwRefreshRate [in]

Refresh rate of the new display mode. Set this value to 0 to request the default refresh rate for the driver.


#### - dwWidth [in]

Width of the new display mode.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_GENERIC</li>
<li>DDERR_INVALIDMODE</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_LOCKEDSURFACES</li>
<li>DDERR_NOEXCLUSIVEMODE</li>
<li>DDERR_SURFACEBUSY</li>
<li>DDERR_UNSUPPORTED</li>
<li>DDERR_UNSUPPORTEDMODE</li>
<li>DDERR_WASSTILLDRAWING</li>
</ul>



## -remarks



This method must be called by the same thread that created the application window.

If another application changes the display mode, the primary surface is lost, and the method returns DDERR_SURFACELOST until the primary surface is recreated to match the new display mode.



As part of the prior-version <b>IDirectDraw</b> interface, this method did not include the <i>dwRefreshRate</i> and <i>dwFlags</i> parameters.



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the <b>SetDisplayMode</b> method.




## -see-also




<a href="https://msdn.microsoft.com/1a1164fe-00c2-4469-8346-f86f7f48781e">IDirectDraw7</a>
 

 


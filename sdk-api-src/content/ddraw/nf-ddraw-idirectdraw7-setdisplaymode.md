---
UID: NF:ddraw.IDirectDraw7.SetDisplayMode
title: IDirectDraw7::SetDisplayMode (ddraw.h)
author: windows-sdk-content
description: Sets the mode of the display-device hardware.
old-location: directdraw\idirectdraw7_setdisplaymode.htm
tech.root: directdraw
ms.assetid: 385918cd-64f1-449c-822a-0034a8184fb9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDirectDraw7 interface [DirectDraw],SetDisplayMode method, IDirectDraw7.SetDisplayMode, IDirectDraw7::SetDisplayMode, SetDisplayMode, SetDisplayMode method [DirectDraw], SetDisplayMode method [DirectDraw],IDirectDraw7 interface, ddraw/IDirectDraw7::SetDisplayMode, directdraw.idirectdraw7_setdisplaymode
ms.topic: method
f1_keywords: ["ddraw/IDirectDraw7.SetDisplayMode"]
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
 - IDirectDraw7.SetDisplayMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectDraw7::SetDisplayMode


## -description


Sets the mode of the display-device hardware.


## -parameters




### -param arg1 [in]

Width of the new display mode.


### -param arg2 [in]

Height of the new display mode.


### -param arg3 [in]

Bits per pixel (bpp) of the new display mode.


### -param arg4 [in]

Refresh rate of the new display mode. Set this value to 0 to request the default refresh rate for the driver.


### -param arg5 [in]

This value consists of flags that describe additional options. Currently, the only valid flag is DDSDM_STANDARDVGAMODE, which causes the method to set Mode 13, instead of Mode X 320x200x8 mode. If you are setting another resolution, bit depth, or a Mode X mode, do not use this flag; instead, set the parameter to 0.


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



You must use <a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> to access the <b>SetDisplayMode</b> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nn-ddraw-idirectdraw7">IDirectDraw7</a>
 

 


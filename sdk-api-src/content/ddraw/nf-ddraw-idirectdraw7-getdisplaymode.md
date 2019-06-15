---
UID: NF:ddraw.IDirectDraw7.GetDisplayMode
title: IDirectDraw7::GetDisplayMode (ddraw.h)
author: windows-sdk-content
description: Retrieves the current display mode.
old-location: directdraw\idirectdraw7_getdisplaymode.htm
tech.root: directdraw
ms.assetid: bd31efc8-17c4-4744-a03b-a22a50c7d9c2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetDisplayMode, GetDisplayMode method [DirectDraw], GetDisplayMode method [DirectDraw],IDirectDraw7 interface, IDirectDraw7 interface [DirectDraw],GetDisplayMode method, IDirectDraw7.GetDisplayMode, IDirectDraw7::GetDisplayMode, ddraw/IDirectDraw7::GetDisplayMode, directdraw.idirectdraw7_getdisplaymode
ms.topic: method
f1_keywords: ["ddraw/IDirectDraw7.GetDisplayMode"]
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
 - IDirectDraw7.GetDisplayMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectDraw7::GetDisplayMode


## -description


Retrieves the current display mode.


## -parameters






#### - lpDDSurfaceDesc2 [in]

A pointer to a <a href="https://docs.microsoft.com/previous-versions/windows/hardware/drivers/ff550340(v=vs.85)">DDSURFACEDESC2</a> structure that receives a description of the current surface.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_UNSUPPORTEDMODE</li>
</ul>



## -remarks



An application should not save the information that <b>GetDisplayMode</b> returns to restore the display mode on clean-up. The application should instead use the <a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-restoredisplaymode">IDirectDraw7::RestoreDisplayMode</a> method to restore the mode on clean-up, thus avoiding mode-setting conflicts that could arise in a multiprocess environment.

You must use <a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> to access the  <b>GetDisplayMode</b> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nn-ddraw-idirectdraw7">IDirectDraw7</a>
 

 


---
UID: NF:ddraw.IDirectDraw7.GetDisplayMode
title: IDirectDraw7::GetDisplayMode
author: windows-sdk-content
description: Retrieves the current display mode.
old-location: directdraw\idirectdraw7_getdisplaymode.htm
old-project: directdraw
ms.assetid: bd31efc8-17c4-4744-a03b-a22a50c7d9c2
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: GetDisplayMode, GetDisplayMode method [DirectDraw], GetDisplayMode method [DirectDraw],IDirectDraw7 interface, IDirectDraw7 interface [DirectDraw],GetDisplayMode method, IDirectDraw7.GetDisplayMode, IDirectDraw7::GetDisplayMode, ddraw/IDirectDraw7::GetDisplayMode, directdraw.idirectdraw7_getdisplaymode
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
 - IDirectDraw7.GetDisplayMode
product: Windows
targetos: Windows
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
---

# IDirectDraw7::GetDisplayMode


## -description


Retrieves the current display mode.


## -parameters






#### - lpDDSurfaceDesc2 [in]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550340">DDSURFACEDESC2</a> structure that receives a description of the current surface.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_UNSUPPORTEDMODE</li>
</ul>



## -remarks



An application should not save the information that <b>GetDisplayMode</b> returns to restore the display mode on clean-up. The application should instead use the <a href="https://msdn.microsoft.com/7538339a-8886-4b40-9779-17c8ebe81446">IDirectDraw7::RestoreDisplayMode</a> method to restore the mode on clean-up, thus avoiding mode-setting conflicts that could arise in a multiprocess environment.

You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the  <b>GetDisplayMode</b> method.




## -see-also




<a href="https://msdn.microsoft.com/1a1164fe-00c2-4469-8346-f86f7f48781e">IDirectDraw7</a>
 

 


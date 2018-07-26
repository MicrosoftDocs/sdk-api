---
UID: NF:ddraw.IDirectDrawSurface7.GetCaps
title: IDirectDrawSurface7::GetCaps
author: windows-sdk-content
description: Retrieves the capabilities of this surface. These capabilities are not necessarily related to the capabilities of the display device.
old-location: directdraw\idirectdrawsurface7_getcaps.htm
old-project: directdraw
ms.assetid: 971290b7-7df6-41c7-8197-b6169ddd092b
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: GetCaps, GetCaps method [DirectDraw], GetCaps method [DirectDraw],IDirectDrawSurface7 interface, IDirectDrawSurface7 interface [DirectDraw],GetCaps method, IDirectDrawSurface7.GetCaps, IDirectDrawSurface7::GetCaps, ddraw/IDirectDrawSurface7::GetCaps, directdraw.idirectdrawsurface7_getcaps
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
 - IDirectDrawSurface7.GetCaps
product: Windows
targetos: Windows
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
---

# IDirectDrawSurface7::GetCaps


## -description


Retrieves the capabilities of this surface. These capabilities are not necessarily related to the capabilities of the display device.


## -parameters






#### - lpDDSCaps [in]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550292">DDSCAPS2</a> structure that receives the hardware capabilities of this surface.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
</ul>



## -remarks



The <b>IDirectDrawSurface7::GetCaps</b> method differs from its counterpart in the <b>IDirectDrawSurface3</b> interface in that it accepts a pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550292">DDSCAPS2</a> structure, rather than the legacy <a href="https://msdn.microsoft.com/library/windows/hardware/ff550286">DDSCAPS</a> structure.



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the  <b>GetCaps</b> method.




## -see-also




<a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a>
 

 


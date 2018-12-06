---
UID: NF:ddraw.IDirectDrawSurface7.GetFlipStatus
title: IDirectDrawSurface7::GetFlipStatus
author: windows-sdk-content
description: Retrieves status about whether this surface has finished its flipping process.
old-location: directdraw\idirectdrawsurface7_getflipstatus.htm
tech.root: directdraw
ms.assetid: e337bdde-bf63-414a-88a5-507478476667
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DDGFS_CANFLIP, DDGFS_ISFLIPDONE, GetFlipStatus, GetFlipStatus method [DirectDraw], GetFlipStatus method [DirectDraw],IDirectDrawSurface7 interface, IDirectDrawSurface7 interface [DirectDraw],GetFlipStatus method, IDirectDrawSurface7.GetFlipStatus, IDirectDrawSurface7::GetFlipStatus, ddraw/IDirectDrawSurface7::GetFlipStatus, directdraw.idirectdrawsurface7_getflipstatus
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
 - IDirectDrawSurface7.GetFlipStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectDrawSurface7::GetFlipStatus


## -description


Retrieves status about whether this surface has finished its flipping process.


## -parameters






#### - dwFlags [in]

A value that can be set to one of the following flags:



#### DDGFS_CANFLIP

Inquires whether this surface can be flipped immediately, and returns DD_OK if the flip can be completed.



#### DDGFS_ISFLIPDONE

Inquires whether the flip has finished, and returns DD_OK if the last flip on this surface has completed.


## -returns



If the method succeeds, the return value is DD_OK.

If it fails, the method can return DDERR_WASSTILLDRAWING if the surface has not finished its flipping process, or one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_INVALIDSURFACETYPE</li>
<li>DDERR_SURFACEBUSY</li>
<li>DDERR_SURFACELOST</li>
<li>DDERR_UNSUPPORTED</li>
<li>DDERR_WASSTILLDRAWING</li>
</ul>



## -remarks



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the  <b>GetFlipStatus</b> method.




## -see-also




<a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a>
 

 


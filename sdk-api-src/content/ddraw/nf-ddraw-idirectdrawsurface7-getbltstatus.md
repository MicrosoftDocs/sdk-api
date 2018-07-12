---
UID: NF:ddraw.IDirectDrawSurface7.GetBltStatus
title: IDirectDrawSurface7::GetBltStatus
author: windows-sdk-content
description: Obtains status about a bit block transfer (bitblt) operation.
old-location: directdraw\idirectdrawsurface7_getbltstatus.htm
old-project: directdraw
ms.assetid: 1f446300-065b-47c1-9778-fb4a5b2ea4bd
ms.author: windowssdkdev
ms.date: 06/18/2018
ms.keywords: DDGBS_CANBLT, DDGBS_ISBLTDONE, GetBltStatus, GetBltStatus method [DirectDraw], GetBltStatus method [DirectDraw],IDirectDrawSurface7 interface, IDirectDrawSurface7 interface [DirectDraw],GetBltStatus method, IDirectDrawSurface7.GetBltStatus, IDirectDrawSurface7::GetBltStatus, ddraw/IDirectDrawSurface7::GetBltStatus, directdraw.idirectdrawsurface7_getbltstatus
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
 - IDirectDrawSurface7.GetBltStatus
product: Windows
targetos: Windows
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
---

# IDirectDrawSurface7::GetBltStatus


## -description


Obtains status about a bit block transfer (bitblt) operation.


## -parameters






#### - dwFlags [in]

A value that can be set to one of the following flags:



#### DDGBS_CANBLT

Inquires whether a bitblt that involves this surface can occur immediately, and returns DD_OK if the bitblt can be completed.



#### DDGBS_ISBLTDONE

Inquires whether the bitblt is done, and returns DD_OK if the last bitblt on this surface has completed.


## -returns



If the method succeeds, a bitbltter is present, and the return value is DD_OK.

If it fails, the method returns DDERR_WASSTILLDRAWING if the bitbltter is busy, DDERR_NOBLTHW if there is no bitbltter, or one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_NOBLTHW</li>
<li>DDERR_SURFACEBUSY</li>
<li>DDERR_SURFACELOST</li>
<li>DDERR_UNSUPPORTED</li>
<li>DDERR_WASSTILLDRAWING</li>
</ul>



## -remarks



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the  <b>GetBltStatus</b> method.




## -see-also




<a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a>
 

 


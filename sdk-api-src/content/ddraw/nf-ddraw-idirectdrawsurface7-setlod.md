---
UID: NF:ddraw.IDirectDrawSurface7.SetLOD
title: IDirectDrawSurface7::SetLOD
author: windows-sdk-content
description: Sets the maximum level of detail (LOD) for a managed mipmap surface. This method succeeds only on managed textures.
old-location: directdraw\idirectdrawsurface7_setlod.htm
old-project: directdraw
ms.assetid: 596b700f-9a16-4ed0-9ea8-8a1da7d841ae
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: IDirectDrawSurface7 interface [DirectDraw],SetLOD method, IDirectDrawSurface7.SetLOD, IDirectDrawSurface7::SetLOD, SetLOD, SetLOD method [DirectDraw], SetLOD method [DirectDraw],IDirectDrawSurface7 interface, ddraw/IDirectDrawSurface7::SetLOD, directdraw.idirectdrawsurface7_setlod
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
req.typenames: DEDUP_CONTAINER_EXTENT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Ddraw.dll
api_name:
-	IDirectDrawSurface7.SetLOD
product: Windows
targetos: Windows
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
---

# IDirectDrawSurface7::SetLOD


## -description


Sets the maximum level of detail (LOD) for a managed mipmap surface. This method succeeds only on managed textures.


## -parameters






#### - dwMaxLOD [in]

The maximum LOD value to be set for the mipmap chain if the call succeeds.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
</ul>



## -remarks



Applications can call this method only for managed textures (those surfaces that were created with the DDSCAPS2_TEXTUREMANAGE flag). If you call <b>SetLOD</b> on a nonmanaged texture, <b>SetLOD</b> fails and returns DDERR_INVALIDOBJECT.

<b>SetLOD</b> communicates to the Direct3D texture manager the most detailed mipmap in this chain that it should load into local video memory. For example, in a five-level mipmap chain, if you set <i>dwMaxLOD</i> to 2, the texture manager should load only mipmap levels 2 through 4 into local video memory at any given time. Likewise, if the most detailed mipmap in the chain has the dimensions 256×256, setting the maximum level to 2 means that the largest mipmap ever present in video memory has dimensions 64×64.



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the  <b>SetLOD</b> method.




## -see-also




<a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a>
 

 


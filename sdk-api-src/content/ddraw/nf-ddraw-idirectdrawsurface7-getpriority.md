---
UID: NF:ddraw.IDirectDrawSurface7.GetPriority
title: IDirectDrawSurface7::GetPriority
author: windows-sdk-content
description: Retrieves the texture-management priority for this texture. This method succeeds only on managed textures.
old-location: directdraw\idirectdrawsurface7_getpriority.htm
old-project: directdraw
ms.assetid: 59a47305-92d5-42a3-9ad1-11c80e3744df
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: GetPriority, GetPriority method [DirectDraw], GetPriority method [DirectDraw],IDirectDrawSurface7 interface, IDirectDrawSurface7 interface [DirectDraw],GetPriority method, IDirectDrawSurface7.GetPriority, IDirectDrawSurface7::GetPriority, ddraw/IDirectDrawSurface7::GetPriority, directdraw.idirectdrawsurface7_getpriority
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Ddraw.dll
api_name:
-	IDirectDrawSurface7.GetPriority
product: Windows
targetos: Windows
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
---

# IDirectDrawSurface7::GetPriority


## -description


Retrieves the texture-management priority for this texture. This method succeeds only on managed textures.



## -parameters






#### - lpdwPriority [out]

A pointer to a variable that receives the texture priority if the call succeeds.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the return value is an error. The method returns DDERR_INVALIDOBJECT if the parameter is invalid or if the texture is not managed by Direct3D.






## -remarks



Priorities are used to determine when managed textures are to be removed from memory. A texture assigned a low priority is removed before a texture with a high priority. If two textures have the same priority, the texture that was used more recently is kept in memory; the other texture is removed.



Applications can set and retrieve priorities only for managed textures (those surfaces that were created with the DDSCAPS2_TEXTUREMANAGE flag). If you call <b>GetPriority</b> on a nonmanaged texture, <b>GetPriority</b> fails and returns DDERR_INVALIDOBJECT.

<b>GetPriority</b> was introduced with the <a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a> interface.

You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the  <b>GetPriority</b> method.




## -see-also




<a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a>
 

 


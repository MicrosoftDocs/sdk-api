---
UID: NF:ddraw.IDirectDrawSurface7.EnumOverlayZOrders
title: IDirectDrawSurface7::EnumOverlayZOrders
author: windows-sdk-content
description: Enumerates the overlay surfaces on the specified destination. You can enumerate the overlays in front-to-back or back-to-front order.
old-location: directdraw\idirectdrawsurface7_enumoverlayzorders.htm
old-project: directdraw
ms.assetid: fab3212c-c1af-4119-85ff-108594cc64fa
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: DDENUMOVERLAYZ_BACKTOFRONT, DDENUMOVERLAYZ_FRONTTOBACK, EnumOverlayZOrders, EnumOverlayZOrders method [DirectDraw], EnumOverlayZOrders method [DirectDraw],IDirectDrawSurface7 interface, IDirectDrawSurface7 interface [DirectDraw],EnumOverlayZOrders method, IDirectDrawSurface7.EnumOverlayZOrders, IDirectDrawSurface7::EnumOverlayZOrders, ddraw/IDirectDrawSurface7::EnumOverlayZOrders, directdraw.idirectdrawsurface7_enumoverlayzorders
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
-	IDirectDrawSurface7.EnumOverlayZOrders
product: Windows
targetos: Windows
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
---

# IDirectDrawSurface7::EnumOverlayZOrders


## -description


Enumerates the overlay surfaces on the specified destination. You can enumerate the overlays in front-to-back or back-to-front order.


## -parameters




### -param






#### - dwFlags [in]

A value that can be set to one of the following flags:



#### DDENUMOVERLAYZ_BACKTOFRONT

Enumerates overlays back to front.



#### DDENUMOVERLAYZ_FRONTTOBACK

Enumerates overlays front to back.


#### - lpContext [in]

Address of the user-defined structure to be passed to the callback function for each overlay surface.


#### - lpfnCallback [in]

Address of the <a href="https://msdn.microsoft.com/DA0FBED3-B61F-4CC3-9B6D-132A9F8ECFE0">EnumSurfacesCallback7</a> callback function to be called for each surface to be overlaid on this surface.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
</ul>



## -remarks



<b>EnumOverlayZOrders</b> differs from its counterparts in previous interface versions in that it accepts a pointer to an <a href="https://msdn.microsoft.com/DA0FBED3-B61F-4CC3-9B6D-132A9F8ECFE0">EnumSurfacesCallback7</a> function, rather than an <a href="https://msdn.microsoft.com/4195C266-4F1D-4DD6-935E-78D07ACAA765">EnumSurfacesCallback</a> or <a href="https://msdn.microsoft.com/BC10A26B-50A3-48C5-94D7-B9C9E8FFE768">EnumSurfacesCallback2</a> function.



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the <b>EnumOverlayZOrders</b> method.




## -see-also




<a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a>
 

 


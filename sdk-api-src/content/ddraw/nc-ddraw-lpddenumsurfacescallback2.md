---
UID: NC:ddraw.LPDDENUMSURFACESCALLBACK2
title: LPDDENUMSURFACESCALLBACK2
author: windows-sdk-content
description: Do not use. This callback function is superseded by the EnumSurfacesCallback7 function that is used with the IDirectDraw7::EnumSurfaces, IDirectDrawSurface7::EnumAttachedSurfaces, and IDirectDrawSurface7::EnumOverlayZOrders methods.
old-location: directdraw\enumsurfacescallback2.htm
tech.root: directdraw
ms.assetid: BC10A26B-50A3-48C5-94D7-B9C9E8FFE768
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EnumSurfacesCallback2, EnumSurfacesCallback2 callback function [DirectDraw], LPDDENUMSURFACESCALLBACK2, LPDDENUMSURFACESCALLBACK2 callback, ddraw/EnumSurfacesCallback2, directdraw.enumsurfacescallback2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ddraw.h
api_name:
 - EnumSurfacesCallback2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LPDDENUMSURFACESCALLBACK2 callback function


## -description


Do not use. This callback function is superseded by the <a href="https://msdn.microsoft.com/DA0FBED3-B61F-4CC3-9B6D-132A9F8ECFE0">EnumSurfacesCallback7</a> function that is used with the <a href="https://msdn.microsoft.com/d97135f3-9921-4e0c-b5ba-e4f709a5e32d">IDirectDraw7::EnumSurfaces</a>, <a href="https://msdn.microsoft.com/7f8e9b53-3aff-491c-ab0c-2f414d1ddb27">IDirectDrawSurface7::EnumAttachedSurfaces</a>, and <a href="https://msdn.microsoft.com/fab3212c-c1af-4119-85ff-108594cc64fa">IDirectDrawSurface7::EnumOverlayZOrders</a> methods.




## -parameters




### -param Arg1


### -param Arg2


### -param Arg3








#### - lpContext [in]

A pointer to an application-defined structure to be passed to the callback function each time that the function is called.


#### - lpDDSurface [in]

A pointer to the <b>IDirectDrawSurface4</b> interface of the attached surface.


#### - lpDDSurfaceDesc [in]

A pointer to a <a href="https://msdn.microsoft.com/507c557f-eb3a-429c-a738-8d715e5d71d3">DDSURFACEDESC2</a> structure that describes the attached surface.


## -returns



The callback function returns DDENUMRET_OK to continue the enumeration.

It returns DDENUMRET_CANCEL to stop the enumeration.






## -remarks



You can use the LPDDENUMSURFACESCALLBACK2 data type to declare a variable that can contain a pointer to this callback function.






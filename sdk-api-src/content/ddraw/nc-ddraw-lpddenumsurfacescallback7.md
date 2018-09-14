---
UID: NC:ddraw.LPDDENUMSURFACESCALLBACK7
title: LPDDENUMSURFACESCALLBACK7
author: windows-sdk-content
description: The EnumSurfacesCallback7 function is an application-defined callback function for the IDirectDrawSurface7::EnumAttachedSurfaces and IDirectDrawSurface7::EnumOverlayZOrders methods.
old-location: directdraw\enumsurfacescallback7.htm
tech.root: directdraw
ms.assetid: DA0FBED3-B61F-4CC3-9B6D-132A9F8ECFE0
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: EnumSurfacesCallback7, EnumSurfacesCallback7 callback function [DirectDraw], LPDDENUMSURFACESCALLBACK7, LPDDENUMSURFACESCALLBACK7 callback, ddraw/EnumSurfacesCallback7, directdraw.enumsurfacescallback7
ms.prod: windows
ms.technology: windows-sdk
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
 - EnumSurfacesCallback7
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LPDDENUMSURFACESCALLBACK7 callback function


## -description


The <i>EnumSurfacesCallback7</i> function is an application-defined callback function for the <a href="https://msdn.microsoft.com/7f8e9b53-3aff-491c-ab0c-2f414d1ddb27">IDirectDrawSurface7::EnumAttachedSurfaces</a> and <a href="https://msdn.microsoft.com/fab3212c-c1af-4119-85ff-108594cc64fa">IDirectDrawSurface7::EnumOverlayZOrders</a> methods.


## -parameters




### -param Arg1


### -param Arg2


### -param Arg3








#### - lpContext [in]

A pointer to an application-defined structure to be passed to the callback function each time that the function is called.


#### - lpDDSurface [in]

A pointer to the <a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a> interface of the attached surface.


#### - lpDDSurfaceDesc [in]

A pointer to a <a href="https://msdn.microsoft.com/507c557f-eb3a-429c-a738-8d715e5d71d3">DDSURFACEDESC2</a> structure that describes the attached surface.


## -returns



The callback function returns DDENUMRET_OK to continue the enumeration.

It returns DDENUMRET_CANCEL to stop the enumeration.






## -remarks



You can use the LPDDENUMSURFACESCALLBACK7 data type to declare a variable that can contain a pointer to this callback function.






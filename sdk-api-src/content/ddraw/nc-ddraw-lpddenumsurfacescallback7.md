---
UID: NC:ddraw.LPDDENUMSURFACESCALLBACK7
title: LPDDENUMSURFACESCALLBACK7 (ddraw.h)
description: The EnumSurfacesCallback7 function is an application-defined callback function for the IDirectDrawSurface7::EnumAttachedSurfaces and IDirectDrawSurface7::EnumOverlayZOrders methods.
helpviewer_keywords: ["EnumSurfacesCallback7","EnumSurfacesCallback7 callback function [DirectDraw]","LPDDENUMSURFACESCALLBACK7","LPDDENUMSURFACESCALLBACK7 callback","ddraw/EnumSurfacesCallback7","directdraw.enumsurfacescallback7"]
old-location: directdraw\enumsurfacescallback7.htm
tech.root: directdraw
ms.assetid: DA0FBED3-B61F-4CC3-9B6D-132A9F8ECFE0
ms.date: 12/05/2018
ms.keywords: EnumSurfacesCallback7, EnumSurfacesCallback7 callback function [DirectDraw], LPDDENUMSURFACESCALLBACK7, LPDDENUMSURFACESCALLBACK7 callback, ddraw/EnumSurfacesCallback7, directdraw.enumsurfacescallback7
f1_keywords:
- ddraw/EnumSurfacesCallback7
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

## -description

The <i>EnumSurfacesCallback7</i> function is an application-defined callback function for the <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-enumattachedsurfaces">IDirectDrawSurface7::EnumAttachedSurfaces</a> and <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-enumoverlayzorders">IDirectDrawSurface7::EnumOverlayZOrders</a> methods.

## -parameters

### -param unnamedParam1 [in]

A pointer to the <a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a> interface of the attached surface.

### -param unnamedParam2 [in]

A pointer to a <a href="/previous-versions/windows/hardware/drivers/ff550340(v=vs.85)">DDSURFACEDESC2</a> structure that describes the attached surface.

### -param unnamedParam3 [in]

A pointer to an application-defined structure to be passed to the callback function each time that the function is called.

## -returns

The callback function returns DDENUMRET_OK to continue the enumeration.

It returns DDENUMRET_CANCEL to stop the enumeration.

## -remarks

You can use the LPDDENUMSURFACESCALLBACK7 data type to declare a variable that can contain a pointer to this callback function.
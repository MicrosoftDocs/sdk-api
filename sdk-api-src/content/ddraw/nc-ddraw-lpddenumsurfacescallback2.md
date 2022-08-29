---
UID: NC:ddraw.LPDDENUMSURFACESCALLBACK2
title: LPDDENUMSURFACESCALLBACK2 (ddraw.h)
description: The LPDDENUMSURFACESCALLBACK2 function (ddraw.h) is superseded by the EnumSurfacesCallback7 function.
helpviewer_keywords: ["EnumSurfacesCallback2","EnumSurfacesCallback2 callback function [DirectDraw]","LPDDENUMSURFACESCALLBACK2","LPDDENUMSURFACESCALLBACK2 callback","ddraw/EnumSurfacesCallback2","directdraw.enumsurfacescallback2"]
old-location: directdraw\enumsurfacescallback2.htm
tech.root: directdraw
ms.assetid: BC10A26B-50A3-48C5-94D7-B9C9E8FFE768
ms.date: 08/12/2022
ms.keywords: EnumSurfacesCallback2, EnumSurfacesCallback2 callback function [DirectDraw], LPDDENUMSURFACESCALLBACK2, LPDDENUMSURFACESCALLBACK2 callback, ddraw/EnumSurfacesCallback2, directdraw.enumsurfacescallback2
f1_keywords:
- ddraw/EnumSurfacesCallback2
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
- EnumSurfacesCallback2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

## -description

Do not use. This callback function is superseded by the <a href="/windows/desktop/api/ddraw/nc-ddraw-lpddenumsurfacescallback7">EnumSurfacesCallback7</a> function that is used with the <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-enumsurfaces">IDirectDraw7::EnumSurfaces</a>, <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-enumattachedsurfaces">IDirectDrawSurface7::EnumAttachedSurfaces</a>, and <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-enumoverlayzorders">IDirectDrawSurface7::EnumOverlayZOrders</a> methods.

## -parameters

### -param unnamedParam1 [in]

A pointer to the <b>IDirectDrawSurface4</b> interface of the attached surface.

### -param unnamedParam2 [in]

A pointer to a <a href="/previous-versions/windows/hardware/drivers/ff550340(v=vs.85)">DDSURFACEDESC2</a> structure that describes the attached surface.

### -param unnamedParam3 [in]

A pointer to an application-defined structure to be passed to the callback function each time that the function is called.

## -returns

The callback function returns DDENUMRET_OK to continue the enumeration.

It returns DDENUMRET_CANCEL to stop the enumeration.

## -remarks

You can use the LPDDENUMSURFACESCALLBACK2 data type to declare a variable that can contain a pointer to this callback function.

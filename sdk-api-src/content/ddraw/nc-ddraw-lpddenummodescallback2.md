---
UID: NC:ddraw.LPDDENUMMODESCALLBACK2
title: LPDDENUMMODESCALLBACK2 (ddraw.h)
description: The EnumModesCallback2 function is an application-defined callback function for the IDirectDraw7::EnumDisplayModes method.
helpviewer_keywords: ["EnumModesCallback2","EnumModesCallback2 callback function [DirectDraw]","LPDDENUMMODESCALLBACK2","LPDDENUMMODESCALLBACK2 callback","ddraw/EnumModesCallback2","directdraw.enummodescallback2"]
old-location: directdraw\enummodescallback2.htm
tech.root: directdraw
ms.assetid: 53185A9A-EBA3-4443-8E76-AC85E69B39F2
ms.date: 12/05/2018
ms.keywords: EnumModesCallback2, EnumModesCallback2 callback function [DirectDraw], LPDDENUMMODESCALLBACK2, LPDDENUMMODESCALLBACK2 callback, ddraw/EnumModesCallback2, directdraw.enummodescallback2
f1_keywords:
- ddraw/EnumModesCallback2
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
- EnumModesCallback2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

## -description

The <i>EnumModesCallback2</i> function is an application-defined callback function for the <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-enumdisplaymodes">IDirectDraw7::EnumDisplayModes</a> method.

## -parameters

### -param unnamedParam1 [in]

A pointer to a read-only <a href="/previous-versions/windows/hardware/drivers/ff550340(v=vs.85)">DDSURFACEDESC2</a> structure that provides the monitor frequency and the mode that can be created.

### -param unnamedParam2 [in]

A pointer to an application-defined structure to be passed to the callback function each time that the function is called.

## -returns

The callback function returns DDENUMRET_OK to continue the enumeration.

It returns DDENUMRET_CANCEL to stop the enumeration.

## -remarks

You can use the LPDDENUMMODESCALLBACK2 data type to declare a variable that can contain a pointer to this callback function.
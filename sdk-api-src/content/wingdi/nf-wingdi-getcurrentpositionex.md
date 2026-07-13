---
UID: NF:wingdi.GetCurrentPositionEx
title: GetCurrentPositionEx function (wingdi.h)
description: The GetCurrentPositionEx function retrieves the current position in logical coordinates.
helpviewer_keywords: ["GetCurrentPositionEx","GetCurrentPositionEx function [Windows GDI]","_win32_GetCurrentPositionEx","gdi.getcurrentpositionex","wingdi/GetCurrentPositionEx"]
old-location: gdi\getcurrentpositionex.htm
tech.root: gdi
ms.assetid: 23a5ac58-2b88-42d3-ab02-8edb8ef187cc
ms.date: 12/05/2018
ms.keywords: GetCurrentPositionEx, GetCurrentPositionEx function [Windows GDI], _win32_GetCurrentPositionEx, gdi.getcurrentpositionex, wingdi/GetCurrentPositionEx
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetCurrentPositionEx
 - wingdi/GetCurrentPositionEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - GetCurrentPositionEx
---

# GetCurrentPositionEx function


## -description

The <b>GetCurrentPositionEx</b> function retrieves the current position in logical coordinates.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param lppt [out]

A pointer to a <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure that receives the logical coordinates of the current position.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -see-also

<a href="/windows/desktop/gdi/coordinate-space-and-transformation-functions">Coordinate Space and Transformation Functions</a>



<a href="/windows/desktop/gdi/coordinate-spaces-and-transformations">Coordinate Spaces and Transformations Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-movetoex">MoveToEx</a>



<a href="/windows/win32/api/windef/ns-windef-point">POINT</a>
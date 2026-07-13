---
UID: NF:wingdi.OffsetWindowOrgEx
title: OffsetWindowOrgEx function (wingdi.h)
description: The OffsetWindowOrgEx function modifies the window origin for a device context using the specified horizontal and vertical offsets.
helpviewer_keywords: ["OffsetWindowOrgEx","OffsetWindowOrgEx function [Windows GDI]","_win32_OffsetWindowOrgEx","gdi.offsetwindoworgex","wingdi/OffsetWindowOrgEx"]
old-location: gdi\offsetwindoworgex.htm
tech.root: gdi
ms.assetid: 085f40ac-d91f-4853-8ad1-1fc5da08b981
ms.date: 12/05/2018
ms.keywords: OffsetWindowOrgEx, OffsetWindowOrgEx function [Windows GDI], _win32_OffsetWindowOrgEx, gdi.offsetwindoworgex, wingdi/OffsetWindowOrgEx
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
 - OffsetWindowOrgEx
 - wingdi/OffsetWindowOrgEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - ext-ms-win-gdi-draw-l1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - OffsetWindowOrgEx
---

# OffsetWindowOrgEx function


## -description

The <b>OffsetWindowOrgEx</b> function modifies the window origin for a device context using the specified horizontal and vertical offsets.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param x [in]

The horizontal offset, in logical units.

### -param y [in]

The vertical offset, in logical units.

### -param lppt [out]

A pointer to a <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure. The logical coordinates of the previous window origin are placed in this structure. If <i>lpPoint</i> is <b>NULL</b>, the previous origin is not returned.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -see-also

<a href="/windows/desktop/gdi/coordinate-space-and-transformation-functions">Coordinate Space and Transformation Functions</a>



<a href="/windows/desktop/gdi/coordinate-spaces-and-transformations">Coordinate Spaces and Transformations Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getviewportorgex">GetViewportOrgEx</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-offsetviewportorgex">OffsetViewportOrgEx</a>



<a href="/windows/win32/api/windef/ns-windef-point">POINT</a>
---
UID: NF:wingdi.OffsetViewportOrgEx
title: OffsetViewportOrgEx function (wingdi.h)
description: The OffsetViewportOrgEx function modifies the viewport origin for a device context using the specified horizontal and vertical offsets.
helpviewer_keywords: ["OffsetViewportOrgEx","OffsetViewportOrgEx function [Windows GDI]","_win32_OffsetViewportOrgEx","gdi.offsetviewportorgex","wingdi/OffsetViewportOrgEx"]
old-location: gdi\offsetviewportorgex.htm
tech.root: gdi
ms.assetid: 54311cbe-1c54-4193-8991-891dbd0856bf
ms.date: 12/05/2018
ms.keywords: OffsetViewportOrgEx, OffsetViewportOrgEx function [Windows GDI], _win32_OffsetViewportOrgEx, gdi.offsetviewportorgex, wingdi/OffsetViewportOrgEx
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
 - OffsetViewportOrgEx
 - wingdi/OffsetViewportOrgEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Draw-l1-1-1.dll
 - ext-ms-win-gdi-draw-l1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - OffsetViewportOrgEx
---

# OffsetViewportOrgEx function


## -description

The <b>OffsetViewportOrgEx</b> function modifies the viewport origin for a device context using the specified horizontal and vertical offsets.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param x [in]

The horizontal offset, in device units.

### -param y [in]

The vertical offset, in device units.

### -param lppt [out]

A pointer to a <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure. The previous viewport origin, in device units, is placed in this structure. If <i>lpPoint</i> is <b>NULL</b>, the previous viewport origin is not returned.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The new origin is the sum of the current origin and the horizontal and vertical offsets.

## -see-also

<a href="/windows/desktop/gdi/coordinate-space-and-transformation-functions">Coordinate Space and Transformation Functions</a>



<a href="/windows/desktop/gdi/coordinate-spaces-and-transformations">Coordinate Spaces and Transformations Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getviewportorgex">GetViewportOrgEx</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-offsetwindoworgex">OffsetWindowOrgEx</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setviewportorgex">SetViewportOrgEx</a>
---
UID: NF:wingdi.SetWindowOrgEx
title: SetWindowOrgEx function (wingdi.h)
description: The SetWindowOrgEx function specifies which window point maps to the viewport origin (0,0).
helpviewer_keywords: ["SetWindowOrgEx","SetWindowOrgEx function [Windows GDI]","_win32_SetWindowOrgEx","gdi.setwindoworgex","wingdi/SetWindowOrgEx"]
old-location: gdi\setwindoworgex.htm
tech.root: gdi
ms.assetid: 75409b5a-c003-49f2-aceb-a28330b92b0a
ms.date: 12/05/2018
ms.keywords: SetWindowOrgEx, SetWindowOrgEx function [Windows GDI], _win32_SetWindowOrgEx, gdi.setwindoworgex, wingdi/SetWindowOrgEx
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
 - SetWindowOrgEx
 - wingdi/SetWindowOrgEx
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
 - SetWindowOrgEx
---

# SetWindowOrgEx function


## -description

The <b>SetWindowOrgEx</b> function specifies which window point maps to the viewport origin (0,0).

## -parameters

### -param hdc [in]

A handle to the device context.

### -param x [in]

The x-coordinate, in logical units, of the new window origin.

### -param y [in]

The y-coordinate, in logical units, of the new window origin.

### -param lppt [out]

A pointer to a <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure that receives the previous origin of the window, in logical units. If <i>lpPoint</i> is <b>NULL</b>, this parameter is not used.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

This helps define the mapping from the logical coordinate space (also known as a <i>window</i>) to the device coordinate space (the <i>viewport</i>). <b>SetWindowOrgEx</b> specifies which logical point maps to the device point (0,0). It has the effect of shifting the axes so that the logical point (0,0) no longer refers to the upper-left corner.


```cpp

//map the logical point (xWinOrg, yWinOrg) to the device point (0,0) 
SetWindowOrgEx (hdc, xWinOrg, yWinOrg, NULL)

```


This is related to the <a href="/windows/desktop/api/wingdi/nf-wingdi-setviewportorgex">SetViewportOrgEx</a> function. Generally, you will use one function or the other, but not both. Regardless of your use of <b>SetWindowOrgEx</b> and <b>SetViewportOrgEx</b>, the device point (0,0) is always the upper-left corner.

## -see-also

<a href="/windows/desktop/gdi/coordinate-space-and-transformation-functions">Coordinate Space and Transformation Functions</a>



<a href="/windows/desktop/gdi/coordinate-spaces-and-transformations">Coordinate Spaces and Transformations Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getviewportorgex">GetViewportOrgEx</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getwindoworgex">GetWindowOrgEx</a>



<a href="/windows/win32/api/windef/ns-windef-point">POINT</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setviewportorgex">SetViewportOrgEx</a>
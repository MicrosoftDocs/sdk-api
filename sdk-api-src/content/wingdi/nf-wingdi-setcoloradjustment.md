---
UID: NF:wingdi.SetColorAdjustment
title: SetColorAdjustment function (wingdi.h)
description: The SetColorAdjustment function sets the color adjustment values for a device context (DC) using the specified values.
helpviewer_keywords: ["SetColorAdjustment","SetColorAdjustment function [Windows GDI]","_win32_SetColorAdjustment","gdi.setcoloradjustment","wingdi/SetColorAdjustment"]
old-location: gdi\setcoloradjustment.htm
tech.root: gdi
ms.assetid: 292d6cdc-cafa-438a-9392-a9c22e7d44a5
ms.date: 12/05/2018
ms.keywords: SetColorAdjustment, SetColorAdjustment function [Windows GDI], _win32_SetColorAdjustment, gdi.setcoloradjustment, wingdi/SetColorAdjustment
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
 - SetColorAdjustment
 - wingdi/SetColorAdjustment
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
 - SetColorAdjustment
---

# SetColorAdjustment function


## -description

The <b>SetColorAdjustment</b> function sets the color adjustment values for a device context (DC) using the specified values.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param lpca [in]

A pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-coloradjustment">COLORADJUSTMENT</a> structure containing the color adjustment values.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The color adjustment values are used to adjust the input color of the source bitmap for calls to the <a href="/windows/desktop/api/wingdi/nf-wingdi-stretchblt">StretchBlt</a> and <a href="/windows/desktop/api/wingdi/nf-wingdi-stretchdibits">StretchDIBits</a> functions when HALFTONE mode is set.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-coloradjustment">COLORADJUSTMENT</a>



<a href="/windows/desktop/gdi/color-functions">Color Functions</a>



<a href="/windows/desktop/gdi/colors">Colors Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getcoloradjustment">GetColorAdjustment</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setstretchbltmode">SetStretchBltMode</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-stretchblt">StretchBlt</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-stretchdibits">StretchDIBits</a>
---
UID: NF:wingdi.CreateBrushIndirect
title: CreateBrushIndirect function (wingdi.h)
description: The CreateBrushIndirect function creates a logical brush that has the specified style, color, and pattern.
helpviewer_keywords: ["CreateBrushIndirect","CreateBrushIndirect function [Windows GDI]","_win32_CreateBrushIndirect","gdi.createbrushindirect","wingdi/CreateBrushIndirect"]
old-location: gdi\createbrushindirect.htm
tech.root: gdi
ms.assetid: 75f94ad1-ca25-4ad1-9e8c-ad1a4b8475a7
ms.date: 12/05/2018
ms.keywords: CreateBrushIndirect, CreateBrushIndirect function [Windows GDI], _win32_CreateBrushIndirect, gdi.createbrushindirect, wingdi/CreateBrushIndirect
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
 - CreateBrushIndirect
 - wingdi/CreateBrushIndirect
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
 - CreateBrushIndirect
---

# CreateBrushIndirect function


## -description

The <b>CreateBrushIndirect</b> function creates a logical brush that has the specified style, color, and pattern.

## -parameters

### -param plbrush [in]

A pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-logbrush">LOGBRUSH</a> structure that contains information about the brush.

## -returns

If the function succeeds, the return value identifies a logical brush.

If the function fails, the return value is <b>NULL</b>.

## -remarks

A brush is a bitmap that the system uses to paint the interiors of filled shapes.

After an application creates a brush by calling <b>CreateBrushIndirect</b>, it can select it into any device context by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-selectobject">SelectObject</a> function.

A brush created by using a monochrome bitmap (one color plane, one bit per pixel) is drawn using the current text and background colors. Pixels represented by a bit set to 0 are drawn with the current text color; pixels represented by a bit set to 1 are drawn with the current background color.

When you no longer need the brush, call the <a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a> function to delete it.

<b>ICM:</b> No color is done at brush creation. However, color management is performed when the brush is selected into an ICM-enabled device context.

## -see-also

<a href="/windows/desktop/gdi/brush-functions">Brush Functions</a>



<a href="/windows/desktop/gdi/brushes">Brushes Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getbrushorgex">GetBrushOrgEx</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-logbrush">LOGBRUSH</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-selectobject">SelectObject</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setbrushorgex">SetBrushOrgEx</a>
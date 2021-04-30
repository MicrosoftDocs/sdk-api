---
UID: NF:wingdi.PtVisible
title: PtVisible function (wingdi.h)
description: The PtVisible function determines whether the specified point is within the clipping region of a device context.
helpviewer_keywords: ["PtVisible","PtVisible function [Windows GDI]","_win32_PtVisible","gdi.ptvisible","wingdi/PtVisible"]
old-location: gdi\ptvisible.htm
tech.root: gdi
ms.assetid: 72ccbd0f-f85b-434d-b0fc-dbe26348a74d
ms.date: 12/05/2018
ms.keywords: PtVisible, PtVisible function [Windows GDI], _win32_PtVisible, gdi.ptvisible, wingdi/PtVisible
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
 - PtVisible
 - wingdi/PtVisible
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
 - PtVisible
---

# PtVisible function


## -description

The <b>PtVisible</b> function determines whether the specified point is within the clipping region of a device context.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param x [in]

The x-coordinate, in logical units, of the point.

### -param y [in]

The y-coordinate, in logical units, of the point.

## -returns

If the specified point is within the clipping region of the device context, the return value is <b>TRUE</b>(1).

If the specified point is not within the clipping region of the device context, the return value is <b>FALSE</b>(0).

If the <b>HDC</b> is not valid, the return value is (BOOL)-1.

## -see-also

<a href="/windows/desktop/gdi/clipping-functions">Clipping Functions</a>



<a href="/windows/desktop/gdi/clipping">Clipping Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-rectvisible">RectVisible</a>
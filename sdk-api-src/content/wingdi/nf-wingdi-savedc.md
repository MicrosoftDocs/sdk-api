---
UID: NF:wingdi.SaveDC
title: SaveDC function (wingdi.h)
description: The SaveDC function saves the current state of the specified device context (DC) by copying data describing selected objects and graphic modes (such as the bitmap, brush, palette, font, pen, region, drawing mode, and mapping mode) to a context stack.
helpviewer_keywords: ["SaveDC","SaveDC function [Windows GDI]","_win32_SaveDC","gdi.savedc","wingdi/SaveDC"]
old-location: gdi\savedc.htm
tech.root: gdi
ms.assetid: f438cd7f-436f-436c-b32e-67f5558740cb
ms.date: 12/05/2018
ms.keywords: SaveDC, SaveDC function [Windows GDI], _win32_SaveDC, gdi.savedc, wingdi/SaveDC
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
 - SaveDC
 - wingdi/SaveDC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-DC-l1-2-0.dll
 - ext-ms-win-gdi-dc-l1-1-0.dll
 - ext-ms-win-gdi-dc-l1-2-1.dll
 - GDI32Full.dll
api_name:
 - SaveDC
---

# SaveDC function


## -description

The <b>SaveDC</b> function saves the current state of the specified device context (DC) by copying data describing selected objects and graphic modes (such as the bitmap, brush, palette, font, pen, region, drawing mode, and mapping mode) to a context stack.

## -parameters

### -param hdc [in]

A handle to the DC whose state is to be saved.

## -returns

If the function succeeds, the return value identifies the saved state.

If the function fails, the return value is zero.

## -remarks

The <b>SaveDC</b> function can be used any number of times to save any number of instances of the DC state.

A saved state can be restored by using the <a href="/windows/desktop/api/wingdi/nf-wingdi-restoredc">RestoreDC</a> function.

## -see-also

<a href="/windows/desktop/gdi/device-context-functions">Device Context Functions</a>



<a href="/windows/desktop/gdi/device-contexts">Device Contexts Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-restoredc">RestoreDC
      </a>
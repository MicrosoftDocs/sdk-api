---
UID: NF:wingdi.GetBkMode
title: GetBkMode function (wingdi.h)
description: The GetBkMode function returns the current background mix mode for a specified device context. The background mix mode of a device context affects text, hatched brushes, and pen styles that are not solid lines.
helpviewer_keywords: ["GetBkMode","GetBkMode function [Windows GDI]","_win32_GetBkMode","gdi.getbkmode","wingdi/GetBkMode"]
old-location: gdi\getbkmode.htm
tech.root: gdi
ms.assetid: 3faedb48-3163-48fd-b26e-712de9c4bfaf
ms.date: 12/05/2018
ms.keywords: GetBkMode, GetBkMode function [Windows GDI], _win32_GetBkMode, gdi.getbkmode, wingdi/GetBkMode
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
 - GetBkMode
 - wingdi/GetBkMode
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
 - GetBkMode
---

# GetBkMode function


## -description

The <b>GetBkMode</b> function returns the current background mix mode for a specified device context. The background mix mode of a device context affects text, hatched brushes, and pen styles that are not solid lines.

## -parameters

### -param hdc [in]

Handle to the device context whose background mode is to be returned.

## -returns

If the function succeeds, the return value specifies the current background mix mode, either OPAQUE or TRANSPARENT.

If the function fails, the return value is zero.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-getbkcolor">GetBkColor</a>



<a href="/windows/desktop/gdi/painting-and-drawing-functions">Painting and Drawing Functions</a>



<a href="/windows/desktop/gdi/painting-and-drawing">Painting and Drawing Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setbkmode">SetBkMode</a>
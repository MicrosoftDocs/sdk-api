---
UID: NF:wingdi.GetGraphicsMode
title: GetGraphicsMode function (wingdi.h)
description: The GetGraphicsMode function retrieves the current graphics mode for the specified device context.
helpviewer_keywords: ["GetGraphicsMode","GetGraphicsMode function [Windows GDI]","_win32_GetGraphicsMode","gdi.getgraphicsmode","wingdi/GetGraphicsMode"]
old-location: gdi\getgraphicsmode.htm
tech.root: gdi
ms.assetid: 62e2960b-d414-4e84-a94f-60b192071402
ms.date: 12/05/2018
ms.keywords: GetGraphicsMode, GetGraphicsMode function [Windows GDI], _win32_GetGraphicsMode, gdi.getgraphicsmode, wingdi/GetGraphicsMode
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
 - GetGraphicsMode
 - wingdi/GetGraphicsMode
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
 - GetGraphicsMode
---

# GetGraphicsMode function


## -description

The <b>GetGraphicsMode</b> function retrieves the current graphics mode for the specified device context.

## -parameters

### -param hdc [in]

A handle to the device context.

## -returns

If the function succeeds, the return value is the current graphics mode. It can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>GM_COMPATIBLE</td>
<td>The current graphics mode is the compatible graphics mode, a mode that is compatible with 16-bit Windows. In this graphics mode, an application cannot set or modify the world transformation for the specified device context. The compatible graphics mode is the default graphics mode.</td>
</tr>
<tr>
<td>GM_ADVANCED</td>
<td>The current graphics mode is the advanced graphics mode, a mode that allows world transformations. In this graphics mode, an application can set or modify the world transformation for the specified device context.</td>
</tr>
</table>
 

Otherwise, the return value is zero.

## -remarks

An application can set the graphics mode for a device context by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-setgraphicsmode">SetGraphicsMode</a> function.

## -see-also

<a href="/windows/desktop/gdi/coordinate-space-and-transformation-functions">Coordinate Space and Transformation Functions</a>



<a href="/windows/desktop/gdi/coordinate-spaces-and-transformations">Coordinate Spaces and Transformations Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setgraphicsmode">SetGraphicsMode</a>
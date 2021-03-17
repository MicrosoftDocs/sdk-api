---
UID: NF:wingdi.GetROP2
title: GetROP2 function (wingdi.h)
description: The GetROP2 function retrieves the foreground mix mode of the specified device context. The mix mode specifies how the pen or interior color and the color already on the screen are combined to yield a new color.
helpviewer_keywords: ["GetROP2","GetROP2 function [Windows GDI]","_win32_GetROP2","gdi.getrop2","wingdi/GetROP2"]
old-location: gdi\getrop2.htm
tech.root: gdi
ms.assetid: ca1930e0-f6f4-44c8-979c-f50881f3c225
ms.date: 12/05/2018
ms.keywords: GetROP2, GetROP2 function [Windows GDI], _win32_GetROP2, gdi.getrop2, wingdi/GetROP2
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
 - GetROP2
 - wingdi/GetROP2
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
 - GetROP2
---

# GetROP2 function


## -description

The <b>GetROP2</b> function retrieves the foreground mix mode of the specified device context. The mix mode specifies how the pen or interior color and the color already on the screen are combined to yield a new color.

## -parameters

### -param hdc [in]

Handle to the device context.

## -returns

If the function succeeds, the return value specifies the foreground mix mode.

If the function fails, the return value is zero.

## -remarks

Following are the foreground mix modes.

<table>
<tr>
<th>Mix mode</th>
<th>Description</th>
</tr>
<tr>
<td>R2_BLACK</td>
<td>Pixel is always 0.</td>
</tr>
<tr>
<td>R2_COPYPEN</td>
<td>Pixel is the pen color.</td>
</tr>
<tr>
<td>R2_MASKNOTPEN</td>
<td>Pixel is a combination of the colors common to both the screen and the inverse of the pen.</td>
</tr>
<tr>
<td>R2_MASKPEN</td>
<td>Pixel is a combination of the colors common to both the pen and the screen.</td>
</tr>
<tr>
<td>R2_MASKPENNOT</td>
<td>Pixel is a combination of the colors common to both the pen and the inverse of the screen.</td>
</tr>
<tr>
<td>R2_MERGENOTPEN</td>
<td>Pixel is a combination of the screen color and the inverse of the pen color.</td>
</tr>
<tr>
<td>R2_MERGEPEN</td>
<td>Pixel is a combination of the pen color and the screen color.</td>
</tr>
<tr>
<td>R2_MERGEPENNOT</td>
<td>Pixel is a combination of the pen color and the inverse of the screen color.</td>
</tr>
<tr>
<td>R2_NOP</td>
<td>Pixel remains unchanged.</td>
</tr>
<tr>
<td>R2_NOT</td>
<td>Pixel is the inverse of the screen color.</td>
</tr>
<tr>
<td>R2_NOTCOPYPEN</td>
<td>Pixel is the inverse of the pen color.</td>
</tr>
<tr>
<td>R2_NOTMASKPEN</td>
<td>Pixel is the inverse of the R2_MASKPEN color.</td>
</tr>
<tr>
<td>R2_NOTMERGEPEN</td>
<td>Pixel is the inverse of the R2_MERGEPEN color.</td>
</tr>
<tr>
<td>R2_NOTXORPEN</td>
<td>Pixel is the inverse of the R2_XORPEN color.</td>
</tr>
<tr>
<td>R2_WHITE</td>
<td>Pixel is always 1.</td>
</tr>
<tr>
<td>R2_XORPEN</td>
<td>Pixel is a combination of the colors in the pen and in the screen, but not in both.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/gdi/painting-and-drawing-functions">Painting and Drawing Functions</a>



<a href="/windows/desktop/gdi/painting-and-drawing">Painting and Drawing Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setrop2">SetROP2</a>
---
UID: NF:wingdi.GetObjectType
title: GetObjectType function (wingdi.h)
description: The GetObjectType retrieves the type of the specified object.
helpviewer_keywords: ["GetObjectType","GetObjectType function [Windows GDI]","_win32_GetObjectType","gdi.getobjecttype","wingdi/GetObjectType"]
old-location: gdi\getobjecttype.htm
tech.root: gdi
ms.assetid: 334a2c95-3bf4-44dc-abce-df3a3a2d37a8
ms.date: 12/05/2018
ms.keywords: GetObjectType, GetObjectType function [Windows GDI], _win32_GetObjectType, gdi.getobjecttype, wingdi/GetObjectType
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
 - GetObjectType
 - wingdi/GetObjectType
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
 - GetObjectType
---

# GetObjectType function


## -description

The <b>GetObjectType</b> retrieves the type of the specified object.

## -parameters

### -param h [in]

A handle to the graphics object.

## -returns

If the function succeeds, the return value identifies the object. This value can be one of the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>OBJ_BITMAP</td>
<td>Bitmap</td>
</tr>
<tr>
<td>OBJ_BRUSH</td>
<td>Brush</td>
</tr>
<tr>
<td>OBJ_COLORSPACE</td>
<td>Color space</td>
</tr>
<tr>
<td>OBJ_DC</td>
<td>Device context</td>
</tr>
<tr>
<td>OBJ_ENHMETADC</td>
<td>Enhanced metafile DC</td>
</tr>
<tr>
<td>OBJ_ENHMETAFILE</td>
<td>Enhanced metafile</td>
</tr>
<tr>
<td>OBJ_EXTPEN</td>
<td>Extended pen</td>
</tr>
<tr>
<td>OBJ_FONT</td>
<td>Font</td>
</tr>
<tr>
<td>OBJ_MEMDC</td>
<td>Memory DC</td>
</tr>
<tr>
<td>OBJ_METAFILE</td>
<td>Metafile</td>
</tr>
<tr>
<td>OBJ_METADC</td>
<td>Metafile DC</td>
</tr>
<tr>
<td>OBJ_PAL</td>
<td>Palette</td>
</tr>
<tr>
<td>OBJ_PEN</td>
<td>Pen</td>
</tr>
<tr>
<td>OBJ_REGION</td>
<td>Region</td>
</tr>
</table>
 

If the function fails, the return value is zero.

## -see-also

<a href="/windows/desktop/gdi/device-context-functions">Device Context Functions</a>



<a href="/windows/desktop/gdi/device-contexts">Device Contexts Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getobject">GetObject</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-selectobject">SelectObject</a>
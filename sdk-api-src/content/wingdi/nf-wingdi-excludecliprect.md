---
UID: NF:wingdi.ExcludeClipRect
title: ExcludeClipRect function (wingdi.h)
description: The ExcludeClipRect function creates a new clipping region that consists of the existing clipping region minus the specified rectangle.
helpviewer_keywords: ["ExcludeClipRect","ExcludeClipRect function [Windows GDI]","_win32_ExcludeClipRect","gdi.excludecliprect","wingdi/ExcludeClipRect"]
old-location: gdi\excludecliprect.htm
tech.root: gdi
ms.assetid: 5b29c44a-3959-498e-8327-c42ef16a8609
ms.date: 12/05/2018
ms.keywords: ExcludeClipRect, ExcludeClipRect function [Windows GDI], _win32_ExcludeClipRect, gdi.excludecliprect, wingdi/ExcludeClipRect
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
 - ExcludeClipRect
 - wingdi/ExcludeClipRect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - ext-ms-win-gdi-clipping-l1-1-0.dll
 - GDI32Full.dll
api_name:
 - ExcludeClipRect
---

# ExcludeClipRect function


## -description

The <b>ExcludeClipRect</b> function creates a new clipping region that consists of the existing clipping region minus the specified rectangle.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param left [in]

The x-coordinate, in logical units, of the upper-left corner of the rectangle.

### -param top [in]

The y-coordinate, in logical units, of the upper-left corner of the rectangle.

### -param right [in]

The x-coordinate, in logical units, of the lower-right corner of the rectangle.

### -param bottom [in]

The y-coordinate, in logical units, of the lower-right corner of the rectangle.

## -returns

The return value specifies the new clipping region's complexity; it can be one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NULLREGION</b></dt>
</dl>
</td>
<td width="60%">
Region is empty.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SIMPLEREGION</b></dt>
</dl>
</td>
<td width="60%">
Region is a single rectangle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>COMPLEXREGION</b></dt>
</dl>
</td>
<td width="60%">
Region is more than one rectangle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR</b></dt>
</dl>
</td>
<td width="60%">
No region was created.

</td>
</tr>
</table>

## -remarks

The lower and right edges of the specified rectangle are not excluded from the clipping region.

## -see-also

<a href="/windows/desktop/gdi/clipping-functions">Clipping Functions</a>



<a href="/windows/desktop/gdi/clipping">Clipping Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-intersectcliprect">IntersectClipRect</a>
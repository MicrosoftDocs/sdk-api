---
UID: NF:wingdi.OffsetClipRgn
title: OffsetClipRgn function (wingdi.h)
description: The OffsetClipRgn function moves the clipping region of a device context by the specified offsets.
helpviewer_keywords: ["OffsetClipRgn","OffsetClipRgn function [Windows GDI]","_win32_OffsetClipRgn","gdi.offsetcliprgn","wingdi/OffsetClipRgn"]
old-location: gdi\offsetcliprgn.htm
tech.root: gdi
ms.assetid: 332ab3f8-6ad3-4bbc-85a3-b0d2a4b07bc5
ms.date: 12/05/2018
ms.keywords: OffsetClipRgn, OffsetClipRgn function [Windows GDI], _win32_OffsetClipRgn, gdi.offsetcliprgn, wingdi/OffsetClipRgn
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
 - OffsetClipRgn
 - wingdi/OffsetClipRgn
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
 - OffsetClipRgn
---

# OffsetClipRgn function


## -description

The <b>OffsetClipRgn</b> function moves the clipping region of a device context by the specified offsets.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param x [in]

The number of logical units to move left or right.

### -param y [in]

The number of logical units to move up or down.

## -returns

The return value specifies the new region's complexity and can be one of the following values.

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
An error occurred. (The current clipping region is unaffected.)

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/gdi/clipping-functions">Clipping Functions</a>



<a href="/windows/desktop/gdi/clipping">Clipping Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-selectcliprgn">SelectClipRgn</a>
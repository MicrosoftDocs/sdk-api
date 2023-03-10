---
UID: NF:wingdi.OffsetRgn
title: OffsetRgn function (wingdi.h)
description: The OffsetRgn function moves a region by the specified offsets.
helpviewer_keywords: ["OffsetRgn","OffsetRgn function [Windows GDI]","_win32_OffsetRgn","gdi.offsetrgn","wingdi/OffsetRgn"]
old-location: gdi\offsetrgn.htm
tech.root: gdi
ms.assetid: 5228c614-3278-4852-a867-7eed57359aef
ms.date: 12/05/2018
ms.keywords: OffsetRgn, OffsetRgn function [Windows GDI], _win32_OffsetRgn, gdi.offsetrgn, wingdi/OffsetRgn
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
 - OffsetRgn
 - wingdi/OffsetRgn
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-RTCore-GDI-rgn-l1-1-0.dll
 - ext-ms-win-rtcore-gdi-rgn-l1-1-1.dll
api_name:
 - OffsetRgn
---

# OffsetRgn function


## -description

The <b>OffsetRgn</b> function moves a region by the specified offsets.

## -parameters

### -param hrgn [in]

Handle to the region to be moved.

### -param x [in]

Specifies the number of logical units to move left or right.

### -param y [in]

Specifies the number of logical units to move up or down.

## -returns

The return value specifies the new region's complexity. It can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>NULLREGION</td>
<td>Region is empty.</td>
</tr>
<tr>
<td>SIMPLEREGION</td>
<td>Region is a single rectangle.</td>
</tr>
<tr>
<td>COMPLEXREGION</td>
<td>Region is more than one rectangle.</td>
</tr>
<tr>
<td>ERROR</td>
<td>An error occurred; region is unaffected.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/gdi/region-functions">Region Functions</a>



<a href="/windows/desktop/gdi/regions">Regions Overview</a>
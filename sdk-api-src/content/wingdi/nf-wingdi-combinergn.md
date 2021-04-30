---
UID: NF:wingdi.CombineRgn
title: CombineRgn function (wingdi.h)
description: The CombineRgn function combines two regions and stores the result in a third region. The two regions are combined according to the specified mode.
helpviewer_keywords: ["CombineRgn","CombineRgn function [Windows GDI]","RGN_AND","RGN_COPY","RGN_DIFF","RGN_OR","RGN_XOR","_win32_CombineRgn","gdi.combinergn","wingdi/CombineRgn"]
old-location: gdi\combinergn.htm
tech.root: gdi
ms.assetid: ef9fc4f3-737e-4c10-a80b-8ae2097c17d1
ms.date: 12/05/2018
ms.keywords: CombineRgn, CombineRgn function [Windows GDI], RGN_AND, RGN_COPY, RGN_DIFF, RGN_OR, RGN_XOR, _win32_CombineRgn, gdi.combinergn, wingdi/CombineRgn
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
 - CombineRgn
 - wingdi/CombineRgn
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
 - api-ms-win-gdi-ie-rgn-l1-1-0.dll
 - ie_shims.dll
 - ext-ms-win-rtcore-gdi-rgn-l1-1-1.dll
api_name:
 - CombineRgn
---

# CombineRgn function


## -description

The <b>CombineRgn</b> function combines two regions and stores the result in a third region. The two regions are combined according to the specified mode.

## -parameters

### -param hrgnDst [in]

A handle to a new region with dimensions defined by combining two other regions. (This region must exist before <b>CombineRgn</b> is called.)

### -param hrgnSrc1 [in]

A handle to the first of two regions to be combined.

### -param hrgnSrc2 [in]

A handle to the second of two regions to be combined.

### -param iMode [in]

A mode indicating how the two regions will be combined. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RGN_AND"></a><a id="rgn_and"></a><dl>
<dt><b>RGN_AND</b></dt>
</dl>
</td>
<td width="60%">
Creates the intersection of the two combined regions.

</td>
</tr>
<tr>
<td width="40%"><a id="RGN_COPY"></a><a id="rgn_copy"></a><dl>
<dt><b>RGN_COPY</b></dt>
</dl>
</td>
<td width="60%">
Creates a copy of the region identified by <i>hrgnSrc1</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="RGN_DIFF"></a><a id="rgn_diff"></a><dl>
<dt><b>RGN_DIFF</b></dt>
</dl>
</td>
<td width="60%">
Combines the parts of <i>hrgnSrc1</i> that are not part of <i>hrgnSrc2</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="RGN_OR"></a><a id="rgn_or"></a><dl>
<dt><b>RGN_OR</b></dt>
</dl>
</td>
<td width="60%">
Creates the union of two combined regions.

</td>
</tr>
<tr>
<td width="40%"><a id="RGN_XOR"></a><a id="rgn_xor"></a><dl>
<dt><b>RGN_XOR</b></dt>
</dl>
</td>
<td width="60%">
Creates the union of two combined regions except for any overlapping areas.

</td>
</tr>
</table>

## -returns

The return value specifies the type of the resulting region. It can be one of the following values.

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
The region is empty.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SIMPLEREGION</b></dt>
</dl>
</td>
<td width="60%">
The region is a single rectangle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>COMPLEXREGION</b></dt>
</dl>
</td>
<td width="60%">
The region is more than a single rectangle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR</b></dt>
</dl>
</td>
<td width="60%">
No region is created.

</td>
</tr>
</table>

## -remarks

The three regions need not be distinct. For example, the <i>hrgnSrc1</i> parameter can equal the <i>hrgnDest</i> parameter.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-createellipticrgn">CreateEllipticRgn</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createellipticrgnindirect">CreateEllipticRgnIndirect</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createpolypolygonrgn">CreatePolyPolygonRgn</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createpolygonrgn">CreatePolygonRgn</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createrectrgn">CreateRectRgn</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createrectrgnindirect">CreateRectRgnIndirect</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createroundrectrgn">CreateRoundRectRgn</a>



<a href="/windows/desktop/gdi/region-functions">Region Functions</a>



<a href="/windows/desktop/gdi/regions">Regions Overview</a>
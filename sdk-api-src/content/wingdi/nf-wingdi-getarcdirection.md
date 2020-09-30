---
UID: NF:wingdi.GetArcDirection
title: GetArcDirection function (wingdi.h)
description: The GetArcDirection function retrieves the current arc direction for the specified device context. Arc and rectangle functions use the arc direction.
helpviewer_keywords: ["GetArcDirection","GetArcDirection function [Windows GDI]","_win32_GetArcDirection","gdi.getarcdirection","wingdi/GetArcDirection"]
old-location: gdi\getarcdirection.htm
tech.root: gdi
ms.assetid: 6bf426cd-e028-4568-9e9a-aca58dd69732
ms.date: 12/05/2018
ms.keywords: GetArcDirection, GetArcDirection function [Windows GDI], _win32_GetArcDirection, gdi.getarcdirection, wingdi/GetArcDirection
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
 - GetArcDirection
 - wingdi/GetArcDirection
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
 - GetArcDirection
---

# GetArcDirection function


## -description

The <b>GetArcDirection</b> function retrieves the current arc direction for the specified device context. Arc and rectangle functions use the arc direction.

## -parameters

### -param hdc [in]

Handle to the device context.

## -returns

The return value specifies the current arc direction; it can be any one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>AD_COUNTERCLOCKWISE</td>
<td>Arcs and rectangles are drawn counterclockwise.</td>
</tr>
<tr>
<td>AD_CLOCKWISE</td>
<td>Arcs and rectangles are drawn clockwise.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/gdi/line-and-curve-functions">Line and Curve Functions</a>



<a href="/windows/desktop/gdi/lines-and-curves">Lines and Curves Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setarcdirection">SetArcDirection</a>
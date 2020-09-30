---
UID: NF:wingdi.SetArcDirection
title: SetArcDirection function (wingdi.h)
description: The SetArcDirection sets the drawing direction to be used for arc and rectangle functions.
helpviewer_keywords: ["AD_CLOCKWISE","AD_COUNTERCLOCKWISE","SetArcDirection","SetArcDirection function [Windows GDI]","_win32_SetArcDirection","gdi.setarcdirection","wingdi/SetArcDirection"]
old-location: gdi\setarcdirection.htm
tech.root: gdi
ms.assetid: cec31eb2-cc9d-4384-b973-dd4339b96ed0
ms.date: 12/05/2018
ms.keywords: AD_CLOCKWISE, AD_COUNTERCLOCKWISE, SetArcDirection, SetArcDirection function [Windows GDI], _win32_SetArcDirection, gdi.setarcdirection, wingdi/SetArcDirection
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
 - SetArcDirection
 - wingdi/SetArcDirection
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
 - SetArcDirection
---

# SetArcDirection function


## -description

The <b>SetArcDirection</b> sets the drawing direction to be used for arc and rectangle functions.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param dir [in]

The new arc direction. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AD_COUNTERCLOCKWISE"></a><a id="ad_counterclockwise"></a><dl>
<dt><b>AD_COUNTERCLOCKWISE</b></dt>
</dl>
</td>
<td width="60%">
Figures drawn counterclockwise.

</td>
</tr>
<tr>
<td width="40%"><a id="AD_CLOCKWISE"></a><a id="ad_clockwise"></a><dl>
<dt><b>AD_CLOCKWISE</b></dt>
</dl>
</td>
<td width="60%">
Figures drawn clockwise.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value specifies the old arc direction.

If the function fails, the return value is zero.

## -remarks

The default direction is counterclockwise.

The <b>SetArcDirection</b> function specifies the direction in which the following functions draw:

<ul>
<li>
<a href="/windows/desktop/api/wingdi/nf-wingdi-arc">Arc</a>
</li>
<li>
<a href="/windows/desktop/api/wingdi/nf-wingdi-arcto">ArcTo</a>
</li>
<li>
<a href="/windows/desktop/api/wingdi/nf-wingdi-chord">Chord</a>
</li>
<li>
<a href="/windows/desktop/api/wingdi/nf-wingdi-ellipse">Ellipse</a>
</li>
<li>
<a href="/windows/desktop/api/wingdi/nf-wingdi-pie">Pie</a>
</li>
<li>
<a href="/windows/desktop/api/wingdi/nf-wingdi-rectangle">Rectangle</a>
</li>
<li>
<a href="/windows/desktop/api/wingdi/nf-wingdi-roundrect">RoundRect</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/gdi/line-and-curve-functions">Line and Curve Functions</a>



<a href="/windows/desktop/gdi/lines-and-curves">Lines and Curves Overview</a>
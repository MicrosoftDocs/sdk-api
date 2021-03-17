---
UID: NF:wingdi.SelectClipPath
title: SelectClipPath function (wingdi.h)
description: The SelectClipPath function selects the current path as a clipping region for a device context, combining the new region with any existing clipping region using the specified mode.
helpviewer_keywords: ["RGN_AND","RGN_COPY","RGN_DIFF","RGN_OR","RGN_XOR","SelectClipPath","SelectClipPath function [Windows GDI]","_win32_SelectClipPath","gdi.selectclippath","wingdi/SelectClipPath"]
old-location: gdi\selectclippath.htm
tech.root: gdi
ms.assetid: c5102e1b-ba33-4cce-a4e5-93cf10c1c0bb
ms.date: 12/05/2018
ms.keywords: RGN_AND, RGN_COPY, RGN_DIFF, RGN_OR, RGN_XOR, SelectClipPath, SelectClipPath function [Windows GDI], _win32_SelectClipPath, gdi.selectclippath, wingdi/SelectClipPath
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
 - SelectClipPath
 - wingdi/SelectClipPath
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
 - ext-ms-win-gdi-dc-l1-2-1.dll
 - GDI32Full.dll
api_name:
 - SelectClipPath
---

# SelectClipPath function


## -description

The <b>SelectClipPath</b> function selects the current path as a clipping region for a device context, combining the new region with any existing clipping region using the specified mode.

## -parameters

### -param hdc [in]

A handle to the device context of the path.

### -param mode [in]

The way to use the path. This parameter can be one of the following values.

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
The new clipping region includes the intersection (overlapping areas) of the current clipping region and the current path.

</td>
</tr>
<tr>
<td width="40%"><a id="RGN_COPY"></a><a id="rgn_copy"></a><dl>
<dt><b>RGN_COPY</b></dt>
</dl>
</td>
<td width="60%">
The new clipping region is the current path.

</td>
</tr>
<tr>
<td width="40%"><a id="RGN_DIFF"></a><a id="rgn_diff"></a><dl>
<dt><b>RGN_DIFF</b></dt>
</dl>
</td>
<td width="60%">
The new clipping region includes the areas of the current clipping region with those of the current path excluded.

</td>
</tr>
<tr>
<td width="40%"><a id="RGN_OR"></a><a id="rgn_or"></a><dl>
<dt><b>RGN_OR</b></dt>
</dl>
</td>
<td width="60%">
The new clipping region includes the union (combined areas) of the current clipping region and the current path.

</td>
</tr>
<tr>
<td width="40%"><a id="RGN_XOR"></a><a id="rgn_xor"></a><dl>
<dt><b>RGN_XOR</b></dt>
</dl>
</td>
<td width="60%">
The new clipping region includes the union of the current clipping region and the current path but without the overlapping areas.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The device context identified by the <i>hdc</i> parameter must contain a closed path.


#### Examples

For an example, see <a href="/windows/desktop/gdi/using-clipping">Using Clipping</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-beginpath">BeginPath</a>



<a href="/windows/desktop/gdi/clipping-functions">Clipping Functions</a>



<a href="/windows/desktop/gdi/clipping">Clipping Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-endpath">EndPath</a>
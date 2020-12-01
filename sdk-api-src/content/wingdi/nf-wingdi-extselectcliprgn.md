---
UID: NF:wingdi.ExtSelectClipRgn
title: ExtSelectClipRgn function (wingdi.h)
description: The ExtSelectClipRgn function combines the specified region with the current clipping region using the specified mode.
helpviewer_keywords: ["ExtSelectClipRgn","ExtSelectClipRgn function [Windows GDI]","RGN_AND","RGN_COPY","RGN_DIFF","RGN_OR","RGN_XOR","_win32_ExtSelectClipRgn","gdi.extselectcliprgn","wingdi/ExtSelectClipRgn"]
old-location: gdi\extselectcliprgn.htm
tech.root: gdi
ms.assetid: d222defe-2ef9-4622-b2e1-462a91cb1b0a
ms.date: 12/05/2018
ms.keywords: ExtSelectClipRgn, ExtSelectClipRgn function [Windows GDI], RGN_AND, RGN_COPY, RGN_DIFF, RGN_OR, RGN_XOR, _win32_ExtSelectClipRgn, gdi.extselectcliprgn, wingdi/ExtSelectClipRgn
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
 - ExtSelectClipRgn
 - wingdi/ExtSelectClipRgn
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
api_name:
 - ExtSelectClipRgn
---

# ExtSelectClipRgn function


## -description

The <b>ExtSelectClipRgn</b> function combines the specified region with the current clipping region using the specified mode.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param hrgn [in]

A handle to the region to be selected. This handle must not be <b>NULL</b> unless the RGN_COPY mode is specified.

### -param mode [in]

The operation to be performed. It must be one of the following values.

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
The new clipping region combines the overlapping areas of the current clipping region and the region identified by <i>hrgn</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="RGN_COPY"></a><a id="rgn_copy"></a><dl>
<dt><b>RGN_COPY</b></dt>
</dl>
</td>
<td width="60%">
The new clipping region is a copy of the region identified by <i>hrgn</i>. This is identical to <a href="/windows/desktop/api/wingdi/nf-wingdi-selectcliprgn">SelectClipRgn</a>. If the region identified by <i>hrgn</i> is <b>NULL</b>, the new clipping region is the default clipping region (the default clipping region is a null region).

</td>
</tr>
<tr>
<td width="40%"><a id="RGN_DIFF"></a><a id="rgn_diff"></a><dl>
<dt><b>RGN_DIFF</b></dt>
</dl>
</td>
<td width="60%">
The new clipping region combines the areas of the current clipping region with those areas excluded from the region identified by <i>hrgn</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="RGN_OR"></a><a id="rgn_or"></a><dl>
<dt><b>RGN_OR</b></dt>
</dl>
</td>
<td width="60%">
The new clipping region combines the current clipping region and the region identified by <i>hrgn</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="RGN_XOR"></a><a id="rgn_xor"></a><dl>
<dt><b>RGN_XOR</b></dt>
</dl>
</td>
<td width="60%">
The new clipping region combines the current clipping region and the region identified by <i>hrgn</i> but excludes any overlapping areas.

</td>
</tr>
</table>

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
An error occurred.

</td>
</tr>
</table>

## -remarks

If an error occurs when this function is called, the previous clipping region for the specified device context is not affected.

The <b>ExtSelectClipRgn</b> function assumes that the coordinates for the specified region are specified in device units.

Only a copy of the region identified by the <i>hrgn</i> parameter is used. The region itself can be reused after this call or it can be deleted.

## -see-also

<a href="/windows/desktop/gdi/clipping-functions">Clipping Functions</a>



<a href="/windows/desktop/gdi/clipping">Clipping Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-selectcliprgn">SelectClipRgn</a>
---
UID: NF:wingdi.SelectClipRgn
title: SelectClipRgn function (wingdi.h)
description: The SelectClipRgn function selects a region as the current clipping region for the specified device context.
helpviewer_keywords: ["SelectClipRgn","SelectClipRgn function [Windows GDI]","_win32_SelectClipRgn","gdi.selectcliprgn","wingdi/SelectClipRgn"]
old-location: gdi\selectcliprgn.htm
tech.root: gdi
ms.assetid: 7a4f0b9c-8588-4da8-a030-ed9d8b4ee08d
ms.date: 12/05/2018
ms.keywords: SelectClipRgn, SelectClipRgn function [Windows GDI], _win32_SelectClipRgn, gdi.selectcliprgn, wingdi/SelectClipRgn
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
 - SelectClipRgn
 - wingdi/SelectClipRgn
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-rgn-l1-1-0.dll
 - Ext-MS-Win-RTCore-GDI-rgn-l1-1-0.dll
 - ext-ms-win-rtcore-gdi-rgn-l1-1-1.dll
 - API-MS-Win-GDI-Internal-Uap-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - SelectClipRgn
---

# SelectClipRgn function


## -description

The <b>SelectClipRgn</b> function selects a region as the current clipping region for the specified device context.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param hrgn [in]

A handle to the region to be selected.

## -returns

The return value specifies the region's complexity and can be one of the following values.

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
An error occurred. (The previous clipping region is unaffected.)

</td>
</tr>
</table>

## -remarks

Only a copy of the selected region is used. The region itself can be selected for any number of other device contexts or it can be deleted.

The <b>SelectClipRgn</b> function assumes that the coordinates for a region are specified in device units.

To remove a device-context's clipping region, specify a <b>NULL</b> region handle.


#### Examples

For an example, see <a href="/windows/desktop/gdi/clipping-output">Clipping Output</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/gdi/clipping-functions">Clipping Functions</a>



<a href="/windows/desktop/gdi/clipping">Clipping Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-extselectcliprgn">ExtSelectClipRgn</a>
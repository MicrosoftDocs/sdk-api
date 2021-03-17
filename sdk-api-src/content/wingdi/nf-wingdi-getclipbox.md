---
UID: NF:wingdi.GetClipBox
title: GetClipBox function (wingdi.h)
description: The GetClipBox function retrieves the dimensions of the tightest bounding rectangle that can be drawn around the current visible area on the device.
helpviewer_keywords: ["GetClipBox","GetClipBox function [Windows GDI]","_win32_GetClipBox","gdi.getclipbox","wingdi/GetClipBox"]
old-location: gdi\getclipbox.htm
tech.root: gdi
ms.assetid: b4ee68ab-b99e-48b6-90ce-6d6c0ae144e2
ms.date: 12/05/2018
ms.keywords: GetClipBox, GetClipBox function [Windows GDI], _win32_GetClipBox, gdi.getclipbox, wingdi/GetClipBox
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
 - GetClipBox
 - wingdi/GetClipBox
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
 - GetClipBox
---

# GetClipBox function


## -description

The <b>GetClipBox</b> function retrieves the dimensions of the tightest bounding rectangle that can be drawn around the current visible area on the device. The visible area is defined by the current clipping region or clip path, as well as any overlapping windows.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param lprect [out]

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that is to receive the rectangle dimensions, in logical units.

## -returns

If the function succeeds, the return value specifies the clipping box's complexity and can be one of the following values.

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
 

<b>GetClipBox</b> returns logical coordinates based on the given device context.

## -see-also

<a href="/windows/desktop/gdi/clipping-functions">Clipping Functions</a>



<a href="/windows/desktop/gdi/clipping">Clipping Overview</a>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>
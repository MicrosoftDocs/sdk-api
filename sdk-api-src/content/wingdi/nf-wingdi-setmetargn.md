---
UID: NF:wingdi.SetMetaRgn
title: SetMetaRgn function (wingdi.h)
description: The SetMetaRgn function intersects the current clipping region for the specified device context with the current metaregion and saves the combined region as the new metaregion for the specified device context.
helpviewer_keywords: ["SetMetaRgn","SetMetaRgn function [Windows GDI]","_win32_SetMetaRgn","gdi.setmetargn","wingdi/SetMetaRgn"]
old-location: gdi\setmetargn.htm
tech.root: gdi
ms.assetid: 79f5dc01-bdec-4844-be94-1f9cf5bfd712
ms.date: 12/05/2018
ms.keywords: SetMetaRgn, SetMetaRgn function [Windows GDI], _win32_SetMetaRgn, gdi.setmetargn, wingdi/SetMetaRgn
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
 - SetMetaRgn
 - wingdi/SetMetaRgn
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
 - GDI32Min.dll
api_name:
 - SetMetaRgn
---

# SetMetaRgn function


## -description

The <b>SetMetaRgn</b> function intersects the current clipping region for the specified device context with the current metaregion and saves the combined region as the new metaregion for the specified device context. The clipping region is reset to a null region.

## -parameters

### -param hdc [in]

A handle to the device context.

## -returns

The return value specifies the new clipping region's complexity and can be one of the following values.

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

The current clipping region of a device context is defined by the intersection of its clipping region and its metaregion.

The <b>SetMetaRgn</b> function should only be called after an application's original device context was saved by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-savedc">SaveDC</a> function.

## -see-also

<a href="/windows/desktop/gdi/clipping-functions">Clipping Functions</a>



<a href="/windows/desktop/gdi/clipping">Clipping Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getmetargn">GetMetaRgn</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-savedc">SaveDC</a>
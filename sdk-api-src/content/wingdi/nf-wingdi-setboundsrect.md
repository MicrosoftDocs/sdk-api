---
UID: NF:wingdi.SetBoundsRect
title: SetBoundsRect function (wingdi.h)
description: The SetBoundsRect function controls the accumulation of bounding rectangle information for the specified device context.
helpviewer_keywords: ["DCB_ACCUMULATE","DCB_DISABLE","DCB_ENABLE","DCB_RESET","SetBoundsRect","SetBoundsRect function [Windows GDI]","_win32_SetBoundsRect","gdi.setboundsrect","wingdi/SetBoundsRect"]
old-location: gdi\setboundsrect.htm
tech.root: gdi
ms.assetid: ad361e78-42e8-4945-9395-fab983e396df
ms.date: 12/05/2018
ms.keywords: DCB_ACCUMULATE, DCB_DISABLE, DCB_ENABLE, DCB_RESET, SetBoundsRect, SetBoundsRect function [Windows GDI], _win32_SetBoundsRect, gdi.setboundsrect, wingdi/SetBoundsRect
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
 - SetBoundsRect
 - wingdi/SetBoundsRect
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
 - SetBoundsRect
---

# SetBoundsRect function


## -description

The <b>SetBoundsRect</b> function controls the accumulation of bounding rectangle information for the specified device context. The system can maintain a bounding rectangle for all drawing operations. An application can examine and set this rectangle. The drawing boundaries are useful for invalidating bitmap caches.

## -parameters

### -param hdc [in]

A handle to the device context for which to accumulate bounding rectangles.

### -param lprect [in]

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure used to set the bounding rectangle. Rectangle dimensions are in logical coordinates. This parameter can be <b>NULL</b>.

### -param flags [in]

Specifies how the new rectangle will be combined with the accumulated rectangle. This parameter can be one of more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DCB_ACCUMULATE"></a><a id="dcb_accumulate"></a><dl>
<dt><b>DCB_ACCUMULATE</b></dt>
</dl>
</td>
<td width="60%">
Adds the rectangle specified by the <i>lprcBounds</i> parameter to the bounding rectangle (using a rectangle union operation). Using both DCB_RESET and DCB_ACCUMULATE sets the bounding rectangle to the rectangle specified by the <i>lprcBounds</i> parameter.

</td>
</tr>
<tr>
<td width="40%"><a id="DCB_DISABLE"></a><a id="dcb_disable"></a><dl>
<dt><b>DCB_DISABLE</b></dt>
</dl>
</td>
<td width="60%">
Turns off boundary accumulation.

</td>
</tr>
<tr>
<td width="40%"><a id="DCB_ENABLE"></a><a id="dcb_enable"></a><dl>
<dt><b>DCB_ENABLE</b></dt>
</dl>
</td>
<td width="60%">
Turns on boundary accumulation, which is disabled by default.

</td>
</tr>
<tr>
<td width="40%"><a id="DCB_RESET"></a><a id="dcb_reset"></a><dl>
<dt><b>DCB_RESET</b></dt>
</dl>
</td>
<td width="60%">
Clears the bounding rectangle.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value specifies the previous state of the bounding rectangle. This state can be a combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>DCB_DISABLE</td>
<td>Boundary accumulation is off.</td>
</tr>
<tr>
<td>DCB_ENABLE</td>
<td>Boundary accumulation is on. DCB_ENABLE and DCB_DISABLE are mutually exclusive.</td>
</tr>
<tr>
<td>DCB_RESET</td>
<td>Bounding rectangle is empty.</td>
</tr>
<tr>
<td>DCB_SET</td>
<td>Bounding rectangle is not empty. DCB_SET and DCB_RESET are mutually exclusive.</td>
</tr>
</table>
 

If the function fails, the return value is zero.

## -remarks

The DCB_SET value is a combination of the bit values DCB_ACCUMULATE and DCB_RESET. Applications that check the DCB_RESET bit to determine whether the bounding rectangle is empty must also check the DCB_ACCUMULATE bit. The bounding rectangle is empty only if the DCB_RESET bit is 1 and the DCB_ACCUMULATE bit is 0.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-getboundsrect">GetBoundsRect</a>



<a href="/windows/desktop/gdi/painting-and-drawing-functions">Painting and Drawing Functions</a>



<a href="/windows/desktop/gdi/painting-and-drawing">Painting and Drawing Overview</a>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>
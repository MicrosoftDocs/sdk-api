---
UID: NF:wingdi.PatBlt
title: PatBlt function
author: windows-sdk-content
description: The PatBlt function paints the specified rectangle using the brush that is currently selected into the specified device context. The brush color and the surface color or colors are combined by using the specified raster operation.
old-location: gdi\patblt.htm
tech.root: gdi
ms.assetid: 6deea8ef-b55d-4086-a54e-3f89bb17c6cd
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: BLACKNESS, DSTINVERT, PATCOPY, PATINVERT, PatBlt, PatBlt function [Windows GDI], WHITENESS, _win32_PatBlt, gdi.patblt, wingdi/PatBlt
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Draw-l1-1-1.dll
 - ext-ms-win-gdi-draw-l1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - PatBlt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- PatBlt
: 
---

# PatBlt function


## -description


The <b>PatBlt</b> function paints the specified rectangle using the brush that is currently selected into the specified device context. The brush color and the surface color or colors are combined by using the specified raster operation.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param x [in]

The x-coordinate, in logical units, of the upper-left corner of the rectangle to be filled.


### -param y [in]

The y-coordinate, in logical units, of the upper-left corner of the rectangle to be filled.


### -param w [in]

The width, in logical units, of the rectangle.


### -param h [in]

The height, in logical units, of the rectangle.


### -param rop [in]

The raster operation code. This code can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PATCOPY"></a><a id="patcopy"></a><dl>
<dt><b>PATCOPY</b></dt>
</dl>
</td>
<td width="60%">
Copies the specified pattern into the destination bitmap.

</td>
</tr>
<tr>
<td width="40%"><a id="PATINVERT"></a><a id="patinvert"></a><dl>
<dt><b>PATINVERT</b></dt>
</dl>
</td>
<td width="60%">
Combines the colors of the specified pattern with the colors of the destination rectangle by using the Boolean XOR operator.

</td>
</tr>
<tr>
<td width="40%"><a id="DSTINVERT"></a><a id="dstinvert"></a><dl>
<dt><b>DSTINVERT</b></dt>
</dl>
</td>
<td width="60%">
Inverts the destination rectangle.

</td>
</tr>
<tr>
<td width="40%"><a id="BLACKNESS"></a><a id="blackness"></a><dl>
<dt><b>BLACKNESS</b></dt>
</dl>
</td>
<td width="60%">
Fills the destination rectangle using the color associated with index 0 in the physical palette. (This color is black for the default physical palette.)

</td>
</tr>
<tr>
<td width="40%"><a id="WHITENESS"></a><a id="whiteness"></a><dl>
<dt><b>WHITENESS</b></dt>
</dl>
</td>
<td width="60%">
Fills the destination rectangle using the color associated with index 1 in the physical palette. (This color is white for the default physical palette.)

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The values of the <i>dwRop</i> parameter for this function are a limited subset of the full 256 ternary raster-operation codes; in particular, an operation code that refers to a source rectangle cannot be used.

Not all devices support the <b>PatBlt</b> function. For more information, see the description of the RC_BITBLT capability in the <a href="https://msdn.microsoft.com/d524c4c7-22af-495d-aecc-b9921e53ca7b">GetDeviceCaps</a> function.


#### Examples

For an example, see "Example of Menu-Item Bitmaps" in <a href="https://msdn.microsoft.com/en-us/library/ms647558(v=VS.85).aspx">Using Menus</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/617eb778-876c-4bbb-90da-c5f13359becb">Brush Functions</a>



<a href="https://msdn.microsoft.com/b8912842-87d6-4d97-83ce-53d18cbedc74">Brushes Overview</a>



<a href="https://msdn.microsoft.com/d524c4c7-22af-495d-aecc-b9921e53ca7b">GetDeviceCaps</a>
 

 


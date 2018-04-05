---
UID: NF:wingdi.ExtCreatePen
title: ExtCreatePen function
author: windows-driver-content
description: The ExtCreatePen function creates a logical cosmetic or geometric pen that has the specified style, width, and brush attributes.
old-location: gdi\extcreatepen.htm
old-project: gdi
ms.assetid: a1e81314-4fe6-481f-af96-24ebf56332cf
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: ExtCreatePen, ExtCreatePen function [Windows GDI], PS_ALTERNATE, PS_COSMETIC, PS_DASH, PS_DASHDOT, PS_DASHDOTDOT, PS_DOT, PS_ENDCAP_FLAT, PS_ENDCAP_ROUND, PS_ENDCAP_SQUARE, PS_GEOMETRIC, PS_INSIDEFRAME, PS_JOIN_BEVEL, PS_JOIN_MITER, PS_JOIN_ROUND, PS_NULL, PS_SOLID, PS_USERSTYLE, _win32_ExtCreatePen, gdi.extcreatepen, wingdi/ExtCreatePen
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
req.typenames: FAX_TIME, *PFAX_TIME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	gdi32.dll
-	Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
-	GDI32Full.dll
api_name:
-	ExtCreatePen
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ExtCreatePen function


## -description


The <b>ExtCreatePen</b> function creates a logical cosmetic or geometric pen that has the specified style, width, and brush attributes.


## -parameters




### -param iPenStyle

TBD


### -param cWidth

TBD


### -param plbrush

TBD


### -param cStyle

TBD


### -param pstyle

TBD




#### - dwPenStyle [in]

A combination of type, style, end cap, and join attributes. The values from each category are combined by using the bitwise OR operator ( | ).

The pen type can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PS_GEOMETRIC"></a><a id="ps_geometric"></a><dl>
<dt><b>PS_GEOMETRIC</b></dt>
</dl>
</td>
<td width="60%">
The pen is geometric.

</td>
</tr>
<tr>
<td width="40%"><a id="PS_COSMETIC"></a><a id="ps_cosmetic"></a><dl>
<dt><b>PS_COSMETIC</b></dt>
</dl>
</td>
<td width="60%">
The pen is cosmetic.

</td>
</tr>
</table>
 

The pen style can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PS_ALTERNATE"></a><a id="ps_alternate"></a><dl>
<dt><b>PS_ALTERNATE</b></dt>
</dl>
</td>
<td width="60%">
The pen sets every other pixel. (This style is applicable only for cosmetic pens.)

</td>
</tr>
<tr>
<td width="40%"><a id="PS_SOLID"></a><a id="ps_solid"></a><dl>
<dt><b>PS_SOLID</b></dt>
</dl>
</td>
<td width="60%">
The pen is solid.

</td>
</tr>
<tr>
<td width="40%"><a id="PS_DASH"></a><a id="ps_dash"></a><dl>
<dt><b>PS_DASH</b></dt>
</dl>
</td>
<td width="60%">
The pen is dashed.

</td>
</tr>
<tr>
<td width="40%"><a id="PS_DOT"></a><a id="ps_dot"></a><dl>
<dt><b>PS_DOT</b></dt>
</dl>
</td>
<td width="60%">
The pen is dotted.

</td>
</tr>
<tr>
<td width="40%"><a id="PS_DASHDOT"></a><a id="ps_dashdot"></a><dl>
<dt><b>PS_DASHDOT</b></dt>
</dl>
</td>
<td width="60%">
The pen has alternating dashes and dots.

</td>
</tr>
<tr>
<td width="40%"><a id="PS_DASHDOTDOT"></a><a id="ps_dashdotdot"></a><dl>
<dt><b>PS_DASHDOTDOT</b></dt>
</dl>
</td>
<td width="60%">
The pen has alternating dashes and double dots.

</td>
</tr>
<tr>
<td width="40%"><a id="PS_NULL"></a><a id="ps_null"></a><dl>
<dt><b>PS_NULL</b></dt>
</dl>
</td>
<td width="60%">
The pen is invisible.

</td>
</tr>
<tr>
<td width="40%"><a id="PS_USERSTYLE"></a><a id="ps_userstyle"></a><dl>
<dt><b>PS_USERSTYLE</b></dt>
</dl>
</td>
<td width="60%">
The pen uses a styling array supplied by the user.

</td>
</tr>
<tr>
<td width="40%"><a id="PS_INSIDEFRAME"></a><a id="ps_insideframe"></a><dl>
<dt><b>PS_INSIDEFRAME</b></dt>
</dl>
</td>
<td width="60%">
The pen is solid. When this pen is used in any GDI drawing function that takes a bounding rectangle, the dimensions of the figure are shrunk so that it fits entirely in the bounding rectangle, taking into account the width of the pen. This applies only to geometric pens.

</td>
</tr>
</table>
 

The end cap is only specified for geometric pens. The end cap can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PS_ENDCAP_ROUND"></a><a id="ps_endcap_round"></a><dl>
<dt><b>PS_ENDCAP_ROUND</b></dt>
</dl>
</td>
<td width="60%">
End caps are round.

</td>
</tr>
<tr>
<td width="40%"><a id="PS_ENDCAP_SQUARE"></a><a id="ps_endcap_square"></a><dl>
<dt><b>PS_ENDCAP_SQUARE</b></dt>
</dl>
</td>
<td width="60%">
End caps are square.

</td>
</tr>
<tr>
<td width="40%"><a id="PS_ENDCAP_FLAT"></a><a id="ps_endcap_flat"></a><dl>
<dt><b>PS_ENDCAP_FLAT</b></dt>
</dl>
</td>
<td width="60%">
End caps are flat.

</td>
</tr>
</table>
 

The join is only specified for geometric pens. The join can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PS_JOIN_BEVEL"></a><a id="ps_join_bevel"></a><dl>
<dt><b>PS_JOIN_BEVEL</b></dt>
</dl>
</td>
<td width="60%">
Joins are beveled.

</td>
</tr>
<tr>
<td width="40%"><a id="PS_JOIN_MITER"></a><a id="ps_join_miter"></a><dl>
<dt><b>PS_JOIN_MITER</b></dt>
</dl>
</td>
<td width="60%">
Joins are mitered when they are within the current limit set by the <a href="https://msdn.microsoft.com/4bed113b-9e3f-441f-96d7-71630bf9298e">SetMiterLimit</a> function. If it exceeds this limit, the join is beveled.

</td>
</tr>
<tr>
<td width="40%"><a id="PS_JOIN_ROUND"></a><a id="ps_join_round"></a><dl>
<dt><b>PS_JOIN_ROUND</b></dt>
</dl>
</td>
<td width="60%">
Joins are round.

</td>
</tr>
</table>
 


#### - dwStyleCount [in]

The length, in <b>DWORD</b> units, of the <i>lpStyle</i> array. This value must be zero if <i>dwPenStyle</i> is not PS_USERSTYLE.

The style count is limited to 16.


#### - dwWidth [in]

The width of the pen. If the <i>dwPenStyle</i> parameter is PS_GEOMETRIC, the width is given in logical units. If <i>dwPenStyle</i> is PS_COSMETIC, the width must be set to 1.


#### - lpStyle [in]

A pointer to an array. The first value specifies the length of the first dash in a user-defined style, the second value specifies the length of the first space, and so on. This pointer must be <b>NULL</b> if <i>dwPenStyle</i> is not PS_USERSTYLE.

If the <i>lpStyle</i> array is exceeded during line drawing, the pointer is reset to the beginning of the array. When this happens and <i>dwStyleCount</i> is an even number, the pattern of dashes and spaces repeats. However, if <i>dwStyleCount</i> is odd, the pattern reverses when the pointer is reset -- the first element of <i>lpStyle</i> now refers to spaces, the second refers to dashes, and so forth.


#### - lplb [in]

A pointer to a <a href="https://msdn.microsoft.com/ded2c7a4-2248-4d01-95c6-ab4050719094">LOGBRUSH</a> structure. If <i>dwPenStyle</i> is PS_COSMETIC, the <b>lbColor</b> member specifies the color of the pen and the <b>lpStyle</b> member must be set to BS_SOLID. If <i>dwPenStyle</i> is PS_GEOMETRIC, all members must be used to specify the brush attributes of the pen.


## -returns



If the function succeeds, the return value is a handle that identifies a logical pen.

If the function fails, the return value is zero.




## -remarks



A geometric pen can have any width and can have any of the attributes of a brush, such as dithers and patterns. A cosmetic pen can only be a single pixel wide and must be a solid color, but cosmetic pens are generally faster than geometric pens.

The width of a geometric pen is always specified in world units. The width of a cosmetic pen is always 1.

End caps and joins are only specified for geometric pens.

After an application creates a logical pen, it can select that pen into a device context by calling the <a href="https://msdn.microsoft.com/a89b875e-923d-4048-bc61-8dea132cc56d">SelectObject</a> function. After a pen is selected into a device context, it can be used to draw lines and curves.

If <i>dwPenStyle</i> is PS_COSMETIC and PS_USERSTYLE, the entries in the <i>lpStyle</i> array specify lengths of dashes and spaces in style units. A style unit is defined by the device where the pen is used to draw a line.

If <i>dwPenStyle</i> is PS_GEOMETRIC and PS_USERSTYLE, the entries in the <i>lpStyle</i> array specify lengths of dashes and spaces in logical units.

If <i>dwPenStyle</i> is PS_ALTERNATE, the style unit is ignored and every other pixel is set.

If the <b>lbStyle</b> member of the <a href="https://msdn.microsoft.com/ded2c7a4-2248-4d01-95c6-ab4050719094">LOGBRUSH</a> structure pointed to by <i>lplb</i> is BS_PATTERN, the bitmap pointed to by the <b>lbHatch</b> member of that structure cannot be a DIB section. A DIB section is a bitmap created by <a href="https://msdn.microsoft.com/9276ec84-2860-42be-a9f8-d4efb8d25eec">CreateDIBSection</a>. If that bitmap is a DIB section, the <b>ExtCreatePen</b> function fails.

When an application no longer requires a specified pen, it should call the <a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a> function to delete the pen.

<b>ICM:</b> No color management is done at pen creation. However, color management is performed when the pen is selected into an ICM-enabled device context.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/c60a8e14-400c-40db-869b-b8fea7a03f38">Using Pens</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/9276ec84-2860-42be-a9f8-d4efb8d25eec">CreateDIBSection</a>



<a href="https://msdn.microsoft.com/882facd2-7e06-48f6-82e4-f20e4d5adc92">CreatePen</a>



<a href="https://msdn.microsoft.com/638c0294-9a8f-44ed-a791-1be152cd92dd">CreatePenIndirect</a>



<a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a>



<a href="https://msdn.microsoft.com/555ab876-d990-426d-915c-f98df82a10aa">GetObject</a>



<a href="https://msdn.microsoft.com/ded2c7a4-2248-4d01-95c6-ab4050719094">LOGBRUSH</a>



<a href="https://msdn.microsoft.com/d5cc81b5-0df4-4ec2-8941-d63819a8d5ff">Pen Functions</a>



<a href="https://msdn.microsoft.com/624c3ea6-6e42-4577-9228-961501633937">Pens Overview</a>



<a href="https://msdn.microsoft.com/a89b875e-923d-4048-bc61-8dea132cc56d">SelectObject</a>



<a href="https://msdn.microsoft.com/4bed113b-9e3f-441f-96d7-71630bf9298e">SetMiterLimit</a>
 

 


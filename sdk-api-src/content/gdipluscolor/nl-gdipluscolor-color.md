---
UID: NL:gdipluscolor.Color
title: Color (gdipluscolor.h)
description: A Color object stores a 32-bit value that represents a color.
old-location: gdiplus\_gdiplus_CLASS_Color_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\color.htm
ms.date: 12/05/2018
ms.keywords: Color, Color class [GDI+], Color class [GDI+],described, _gdiplus_CLASS_Color_Class, gdiplus._gdiplus_CLASS_Color_Class, gdipluscolor/Color
ms.topic: class
f1_keywords:
- gdipluscolor/Color
dev_langs:
- c++
req.header: gdipluscolor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- gdipluscolor.h
api_name:
- Color
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Color class


## -description


A <a href="https://docs.microsoft.com/previous-versions/ms536243(v=vs.85)">Color</a> object stores a 32-bit value that represents a color. The color value contains four, 8-bit components: alpha, red, green, and blue. The first 8 bits (the most significant) contain the alpha component, the next 8 bits contain the red component, the next 8 bits contain the green component, and the next 8 bits (the least significant) contain the blue component. The 32-bit value is stored in a variable of type 
			<b>ARGB</b>.

<b xmlns:loc="http://microsoft.com/wdcml/l10n">Color</b> has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Constructors</a></li>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul><h3><a id="constructors"></a>Constructors</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">Color</b> class has these constructors.
<table class="members" id="memberListConstructors">
<tr>
<th align="left" width="37%">Constructor</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolor/nf-gdipluscolor-color-color(inargb)">Color::Color()</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolor/nf-gdipluscolor-color-color(inargb)">Color::Color</a> object and initializes it to opaque black. This is the default constructor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolor/nf-gdipluscolor-color-color(inargb)">Color::Color(ARGB)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolor/nf-gdipluscolor-color-color(inargb)">Color::Color</a> object by using an 
			<b>ARGB</b> value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolor/nf-gdipluscolor-color-color(inbyte_inbyte_inbyte)">Color::Color(BYTE,BYTE,BYTE)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolor/nf-gdipluscolor-color-color(inbyte_inbyte_inbyte)">Color::Color</a> object by using specified values for the red, green, and blue components. This constructor sets the alpha component to 255 (opaque).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolor/nf-gdipluscolor-color-color(inbyte_inbyte_inbyte_inbyte)">Color::Color(BYTE,BYTE,BYTE,BYTE)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolor/nf-gdipluscolor-color-color(inbyte_inbyte_inbyte_inbyte)">Color::Color</a> object by using specified values for the alpha, red, green, and blue components.

</td>
</tr>
</table> 
<h3><a id="methods"></a>Methods</h3>The <b>Color</b> class has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolor/nf-gdipluscolor-color-geta">Color::GetA</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolor/nf-gdipluscolor-color-geta">Color::GetA</a> method gets the alpha component of this <b>Color</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolor/nf-gdipluscolor-color-getalpha">Color::GetAlpha</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolor/nf-gdipluscolor-color-getalpha">Color::GetAlpha</a> method gets the alpha component of this <b>Color</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolor/nf-gdipluscolor-color-getb">Color::GetB</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolor/nf-gdipluscolor-color-getb">Color::GetB</a> method gets the blue component of this <b>Color</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolor/nf-gdipluscolor-color-getblue">Color::GetBlue</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolor/nf-gdipluscolor-color-getblue">Color::GetBlue</a> method gets the blue component of this <b>Color</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolor/nf-gdipluscolor-color-getg">Color::GetG</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolor/nf-gdipluscolor-color-getg">Color::GetG</a> method gets the green component of this <b>Color</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolor/nf-gdipluscolor-color-getgreen">Color::GetGreen</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolor/nf-gdipluscolor-color-getgreen">Color::GetGreen</a> method gets the green component of this <b>Color</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolor/nf-gdipluscolor-color-getr">Color::GetR</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolor/nf-gdipluscolor-color-getr">Color::GetR</a> method gets the red component of this <b>Color</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolor/nf-gdipluscolor-color-getred">Color::GetRed</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolor/nf-gdipluscolor-color-getred">Color::GetRed</a> method gets the red component of this <b>Color</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolor/nf-gdipluscolor-color-getvalue">Color::GetValue</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolor/nf-gdipluscolor-color-getvalue">Color::GetValue</a> method gets the <b>ARGB</b> value of this <b>Color</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolor/nf-gdipluscolor-color-makeargb">Color::MakeARGB</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolor/nf-gdipluscolor-color-makeargb">Color::MakeARGB</a> method creates a 32-bit value that consolidates the specified alpha, red, green, and blue components.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolor/nf-gdipluscolor-color-setfromcolorref">Color::SetFromCOLORREF</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolor/nf-gdipluscolor-color-setfromcolorref">Color::SetFromCOLORREF</a> method uses a GDI<b>COLORREF</b> value to set the <b>ARGB</b> value of this <b>Color</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolor/nf-gdipluscolor-color-setvalue">Color::SetValue</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolor/nf-gdipluscolor-color-setvalue">Color::SetValue</a> method sets the color of this <b>Color</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolor/nf-gdipluscolor-color-tocolorref">Color::ToCOLORREF</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolor/nf-gdipluscolor-color-tocolorref">Color::ToCOLORREF</a> method converts this <b>Color</b> object's <b>ARGB</b> value to a GDI<b>COLORREF</b> value.

</td>
</tr>
</table> 


## -remarks



The alpha component, the most significant 8 bits, specifies the transparency of a color. All four component values range from 0 to 255. An alpha component value of 0 specifies that the color is transparent, and an alpha value of 255 specifies that the color is opaque. Alpha component values from 1 through 254 specify the degree to which the color is blended with the background when the color is rendered. The red, green, and blue color component values range from 0 to 255 and determine the intensity of the color. The <a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolor/nf-gdipluscolor-color-makeargb">Color::MakeARGB</a> method is used to encapsulate the four color components into a single 32-bit value.




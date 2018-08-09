---
UID: NL:gdipluscolor.Color
title: Color
author: windows-sdk-content
description: A Color object stores a 32-bit value that represents a color.
old-location: gdiplus\_gdiplus_CLASS_Color_Class.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\color.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: Color, Color class [GDI+], Color class [GDI+],described, _gdiplus_CLASS_Color_Class, gdiplus._gdiplus_CLASS_Color_Class, gdipluscolor/Color
ms.prod: windows
ms.technology: windows-sdk
ms.topic: class
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - gdipluscolor.h
api_name:
 - Color
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Color class


## -description


A <a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a> object stores a 32-bit value that represents a color. The color value contains four, 8-bit components: alpha, red, green, and blue. The first 8 bits (the most significant) contain the alpha component, the next 8 bits contain the red component, the next 8 bits contain the green component, and the next 8 bits (the least significant) contain the blue component. The 32-bit value is stored in a variable of type 
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
<a href="https://msdn.microsoft.com/en-us/library/ms536259(v=VS.85).aspx">Color::Color()</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/en-us/library/ms536259(v=VS.85).aspx">Color::Color</a> object and initializes it to opaque black. This is the default constructor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms536261(v=VS.85).aspx">Color::Color(ARGB)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/en-us/library/ms536261(v=VS.85).aspx">Color::Color</a> object by using an 
			<b>ARGB</b> value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms536260(v=VS.85).aspx">Color::Color(BYTE,BYTE,BYTE)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/en-us/library/ms536260(v=VS.85).aspx">Color::Color</a> object by using specified values for the red, green, and blue components. This constructor sets the alpha component to 255 (opaque).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms536258(v=VS.85).aspx">Color::Color(BYTE,BYTE,BYTE,BYTE)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/en-us/library/ms536258(v=VS.85).aspx">Color::Color</a> object by using specified values for the alpha, red, green, and blue components.

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
<a href="https://msdn.microsoft.com/en-us/library/ms536245(v=VS.85).aspx">Color::GetA</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms536245(v=VS.85).aspx">Color::GetA</a> method gets the alpha component of this <b>Color</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms536246(v=VS.85).aspx">Color::GetAlpha</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms536246(v=VS.85).aspx">Color::GetAlpha</a> method gets the alpha component of this <b>Color</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms536247(v=VS.85).aspx">Color::GetB</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms536247(v=VS.85).aspx">Color::GetB</a> method gets the blue component of this <b>Color</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms536248(v=VS.85).aspx">Color::GetBlue</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms536248(v=VS.85).aspx">Color::GetBlue</a> method gets the blue component of this <b>Color</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms536249(v=VS.85).aspx">Color::GetG</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms536249(v=VS.85).aspx">Color::GetG</a> method gets the green component of this <b>Color</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms536250(v=VS.85).aspx">Color::GetGreen</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms536250(v=VS.85).aspx">Color::GetGreen</a> method gets the green component of this <b>Color</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms536251(v=VS.85).aspx">Color::GetR</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms536251(v=VS.85).aspx">Color::GetR</a> method gets the red component of this <b>Color</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms536252(v=VS.85).aspx">Color::GetRed</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms536252(v=VS.85).aspx">Color::GetRed</a> method gets the red component of this <b>Color</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms536253(v=VS.85).aspx">Color::GetValue</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms536253(v=VS.85).aspx">Color::GetValue</a> method gets the <b>ARGB</b> value of this <b>Color</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms536254(v=VS.85).aspx">Color::MakeARGB</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms536254(v=VS.85).aspx">Color::MakeARGB</a> method creates a 32-bit value that consolidates the specified alpha, red, green, and blue components.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms536255(v=VS.85).aspx">Color::SetFromCOLORREF</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms536255(v=VS.85).aspx">Color::SetFromCOLORREF</a> method uses a GDI<b>COLORREF</b> value to set the <b>ARGB</b> value of this <b>Color</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms536256(v=VS.85).aspx">Color::SetValue</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms536256(v=VS.85).aspx">Color::SetValue</a> method sets the color of this <b>Color</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms536257(v=VS.85).aspx">Color::ToCOLORREF</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms536257(v=VS.85).aspx">Color::ToCOLORREF</a> method converts this <b>Color</b> object's <b>ARGB</b> value to a GDI<b>COLORREF</b> value.

</td>
</tr>
</table> 


## -remarks



The alpha component, the most significant 8 bits, specifies the transparency of a color. All four component values range from 0 to 255. An alpha component value of 0 specifies that the color is transparent, and an alpha value of 255 specifies that the color is opaque. Alpha component values from 1 through 254 specify the degree to which the color is blended with the background when the color is rendered. The red, green, and blue color component values range from 0 to 255 and determine the intensity of the color. The <a href="https://msdn.microsoft.com/en-us/library/ms536254(v=VS.85).aspx">Color::MakeARGB</a> method is used to encapsulate the four color components into a single 32-bit value.




---
UID: NL:gdipluscolor.Color
title: Color
author: windows-sdk-content
description: A Color object stores a 32-bit value that represents a color.
old-location: gdiplus\_gdiplus_CLASS_Color_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\color.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Color, Color class [GDI+], Color class [GDI+],described, _gdiplus_CLASS_Color_Class, gdiplus._gdiplus_CLASS_Color_Class, gdipluscolor/Color
ms.prod: windows-hardware
ms.technology: windows-devices
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Color class


## -description


A <a href="https://msdn.microsoft.com/ebd68c22-9b00-4a8e-9954-e8b0eda764f8">Color</a> object stores a 32-bit value that represents a color. The color value contains four, 8-bit components: alpha, red, green, and blue. The first 8 bits (the most significant) contain the alpha component, the next 8 bits contain the red component, the next 8 bits contain the green component, and the next 8 bits (the least significant) contain the blue component. The 32-bit value is stored in a variable of type 
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
<a href="https://msdn.microsoft.com/80a95e75-d592-4eed-994c-4e7658d8068c">Color::Color()</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/80a95e75-d592-4eed-994c-4e7658d8068c">Color::Color</a> object and initializes it to opaque black. This is the default constructor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ee941095-77f3-4aee-9478-7b33f625f682">Color::Color(ARGB)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/ee941095-77f3-4aee-9478-7b33f625f682">Color::Color</a> object by using an 
			<b>ARGB</b> value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d7bd27fb-8943-4c6b-acf4-151a5e40e58a">Color::Color(BYTE,BYTE,BYTE)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/d7bd27fb-8943-4c6b-acf4-151a5e40e58a">Color::Color</a> object by using specified values for the red, green, and blue components. This constructor sets the alpha component to 255 (opaque).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2e39f5b6-6fe3-4eb6-b06b-371174400fcc">Color::Color(BYTE,BYTE,BYTE,BYTE)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/2e39f5b6-6fe3-4eb6-b06b-371174400fcc">Color::Color</a> object by using specified values for the alpha, red, green, and blue components.

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
<a href="https://msdn.microsoft.com/e9dcfd1d-a310-4625-a22a-2236d72f1049">Color::GetA</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/e9dcfd1d-a310-4625-a22a-2236d72f1049">Color::GetA</a> method gets the alpha component of this <b>Color</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9b40ba57-88c5-4a8d-9722-256a0bc66a3e">Color::GetAlpha</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/9b40ba57-88c5-4a8d-9722-256a0bc66a3e">Color::GetAlpha</a> method gets the alpha component of this <b>Color</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/09977e61-e46f-48c5-a9b9-5a29f24f15c1">Color::GetB</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/09977e61-e46f-48c5-a9b9-5a29f24f15c1">Color::GetB</a> method gets the blue component of this <b>Color</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/53a42e45-2c2d-40c1-8d22-a954a151f7b6">Color::GetBlue</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/53a42e45-2c2d-40c1-8d22-a954a151f7b6">Color::GetBlue</a> method gets the blue component of this <b>Color</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/254b40cb-d82e-401c-8b46-8bf09ce3914f">Color::GetG</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/254b40cb-d82e-401c-8b46-8bf09ce3914f">Color::GetG</a> method gets the green component of this <b>Color</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b5499194-7078-434e-9d6b-a686ece3fd55">Color::GetGreen</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/b5499194-7078-434e-9d6b-a686ece3fd55">Color::GetGreen</a> method gets the green component of this <b>Color</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/70051577-5f60-4b4c-8d0c-9b285edbd77c">Color::GetR</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/70051577-5f60-4b4c-8d0c-9b285edbd77c">Color::GetR</a> method gets the red component of this <b>Color</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5d2dc63d-14e3-4e38-a41f-1d3e41f07cdd">Color::GetRed</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/5d2dc63d-14e3-4e38-a41f-1d3e41f07cdd">Color::GetRed</a> method gets the red component of this <b>Color</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b333bf7d-b212-43fd-8f86-d7bf73b6a3f4">Color::GetValue</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/b333bf7d-b212-43fd-8f86-d7bf73b6a3f4">Color::GetValue</a> method gets the <b>ARGB</b> value of this <b>Color</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/41befc00-c256-4f56-90c3-8fd5aa18bb49">Color::MakeARGB</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/41befc00-c256-4f56-90c3-8fd5aa18bb49">Color::MakeARGB</a> method creates a 32-bit value that consolidates the specified alpha, red, green, and blue components.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5fb15f81-8bed-4895-bec8-b687028cc5a2">Color::SetFromCOLORREF</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/5fb15f81-8bed-4895-bec8-b687028cc5a2">Color::SetFromCOLORREF</a> method uses a GDI<b>COLORREF</b> value to set the <b>ARGB</b> value of this <b>Color</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/36f95b4e-8f01-4100-ad40-1762291bc069">Color::SetValue</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/36f95b4e-8f01-4100-ad40-1762291bc069">Color::SetValue</a> method sets the color of this <b>Color</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1bf9093d-5316-4280-850e-b0738cf5d0cf">Color::ToCOLORREF</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/1bf9093d-5316-4280-850e-b0738cf5d0cf">Color::ToCOLORREF</a> method converts this <b>Color</b> object's <b>ARGB</b> value to a GDI<b>COLORREF</b> value.

</td>
</tr>
</table> 


## -remarks



The alpha component, the most significant 8 bits, specifies the transparency of a color. All four component values range from 0 to 255. An alpha component value of 0 specifies that the color is transparent, and an alpha value of 255 specifies that the color is opaque. Alpha component values from 1 through 254 specify the degree to which the color is blended with the background when the color is rendered. The red, green, and blue color component values range from 0 to 255 and determine the intensity of the color. The <a href="https://msdn.microsoft.com/41befc00-c256-4f56-90c3-8fd5aa18bb49">Color::MakeARGB</a> method is used to encapsulate the four color components into a single 32-bit value.




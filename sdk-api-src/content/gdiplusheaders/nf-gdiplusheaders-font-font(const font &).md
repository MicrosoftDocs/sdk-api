---
UID: NF:gdiplusheaders.Font.Font(const Font &)
title: Font::Font(const Font &)
author: windows-sdk-content
description: This topic lists the constructors of the Font class. For a complete class listing, see Font Class.
old-location: gdiplus\_gdiplus_CLASS_Font_Constructors.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\fontclass\fontconstructors.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: Font, Font constructors [GDI+], Font.Font, Font.Font(const Font &), Font::Font, Font::Font(const Font &), _gdiplus_CLASS_Font_Constructors, gdiplus._gdiplus_CLASS_Font_Constructors, gdiplusheaders/Font
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplusheaders.h
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
 - HeaderDef
api_location:
 - gdiplusheaders.h
api_name:
 - Font.Font
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Font::Font(const Font &)


## -description


<span>This topic lists the constructors of the 
			<a href="https://msdn.microsoft.com/dd8af524-688c-44dd-b3e4-deadb874bdc3">Font</a> class. For a complete class listing, see <b>Font Class</b>. 
</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Constructor</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72e0513d-867b-4ce4-8fc1-b9f2e755ec41">Font(HDC,HFONT)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/72e0513d-867b-4ce4-8fc1-b9f2e755ec41">Font::Font</a> object indirectly from a GDI logical font by using a handle to a GDI <b>LOGFONT</b> structure.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ce274648-bcde-47ff-9d4e-654a74f029ea">Font(HDC,LOGFONTA*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/ce274648-bcde-47ff-9d4e-654a74f029ea">Font::Font</a> object directly from a GDI logical font. The GDI logical font is a 
			<b>LOGFONTA</b> structure, which is the one-byte character version of a logical font. This constructor is provided for compatibility with GDI.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a8fada4f-7d7d-4737-8718-b1ef5fbae78b">Font(HDC,LOGFONTW*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/a8fada4f-7d7d-4737-8718-b1ef5fbae78b">Font::Font</a> object directly from a GDI logical font. The GDI logical font is a 
			<b>LOGFONTW</b> structure, which is the wide character version of a logical font. This constructor is provided for compatibility with GDI.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72190176-d116-4832-b723-fe2f9baca704">Font(FontFamily*,REAL,INT,Unit)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/72190176-d116-4832-b723-fe2f9baca704">Font::Font</a> object based on a <a href="https://msdn.microsoft.com/cdd2ee9e-eb32-420f-8118-50582b55b7cd">FontFamily</a> object, a size, a font style, and a unit of measurement.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f64bfd9-2ea9-45e6-a0be-2886d89c789e">Font(WCHAR*,REAL,INT,Unit,FontCollection*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/3f64bfd9-2ea9-45e6-a0be-2886d89c789e">Font::Font</a> object based on a font family, a size, a font style, a unit of measurement, and a 
			<a href="https://msdn.microsoft.com/5e1336ea-cb29-4fa4-85d5-077498a69cb2">FontCollection</a> object.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0dabb6fb-172f-4982-bc0d-bb2c122976f8">Font(HDC)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/0dabb6fb-172f-4982-bc0d-bb2c122976f8">Font::Font</a> object based on the GDI font object that is currently selected into a specified device context. This constructor is provided for compatibility with GDI. 

</td>
</tr>
</table>

## -parameters


---
UID: NF:gdiplusheaders.Font.Font(constFont&)
title: Font::Font(const Font &) (gdiplusheaders.h)
description: This topic lists the constructors of the Font class. For a complete class listing, see Font Class. (overload 1/2)
helpviewer_keywords: ["Font","Font constructors [GDI+]","Font.Font","Font.Font(const Font &)","Font::Font","Font::Font(const Font &)","_gdiplus_CLASS_Font_Constructors","gdiplus._gdiplus_CLASS_Font_Constructors","gdiplusheaders/Font"]
old-location: gdiplus\_gdiplus_CLASS_Font_Constructors.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\fontclass\fontconstructors.htm
ms.date: 12/05/2018
ms.keywords: Font, Font constructors [GDI+], Font.Font, Font.Font(const Font &), Font::Font, Font::Font(const Font &), _gdiplus_CLASS_Font_Constructors, gdiplus._gdiplus_CLASS_Font_Constructors, gdiplusheaders/Font
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - Font::Font
 - gdiplusheaders/Font::Font
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - gdiplusheaders.h
api_name:
 - Font.Font
---

# Font::Font(const Font &)


## -description

<span>This topic lists the constructors of the 
			<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font">Font</a> class. For a complete class listing, see <b>Font Class</b>. 
</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Constructor</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconsthfont)">Font(HDC,HFONT)</a>
</td>
<td align="left" width="63%">
Creates a <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconsthfont)">Font::Font</a> object indirectly from a GDI logical font by using a handle to a GDI <b>LOGFONT</b> structure.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/previous-versions/ms536205(v=vs.85)">Font(HDC,LOGFONTA*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="/previous-versions/ms536205(v=vs.85)">Font::Font</a> object directly from a GDI logical font. The GDI logical font is a 
			<b>LOGFONTA</b> structure, which is the one-byte character version of a logical font. This constructor is provided for compatibility with GDI.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/previous-versions/ms536206(v=vs.85)">Font(HDC,LOGFONTW*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="/previous-versions/ms536206(v=vs.85)">Font::Font</a> object directly from a GDI logical font. The GDI logical font is a 
			<b>LOGFONTW</b> structure, which is the wide character version of a logical font. This constructor is provided for compatibility with GDI.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/previous-versions/ms536203(v=vs.85)">Font(FontFamily*,REAL,INT,Unit)</a>
</td>
<td align="left" width="63%">
Creates a <a href="/previous-versions/ms536203(v=vs.85)">Font::Font</a> object based on a <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily">FontFamily</a> object, a size, a font style, and a unit of measurement.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/previous-versions/ms536207(v=vs.85)">Font(WCHAR*,REAL,INT,Unit,FontCollection*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="/previous-versions/ms536207(v=vs.85)">Font::Font</a> object based on a font family, a size, a font style, a unit of measurement, and a 
			<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontcollection">FontCollection</a> object.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc)">Font(HDC)</a>
</td>
<td align="left" width="63%">
Creates a <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc)">Font::Font</a> object based on the GDI font object that is currently selected into a specified device context. This constructor is provided for compatibility with GDI. 

</td>
</tr>
</table>

## -parameters

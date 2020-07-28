---
UID: NF:gdiplusheaders.Font.Font(INconstWCHAR,INREAL,ININT,INUnit,INconstFontCollection)
title: Font::Font(IN const WCHAR,IN REAL,IN INT,IN Unit,IN const FontCollection) (gdiplusheaders.h)
description: Creates a Font::Font object based on a font family, a size, a font style, a unit of measurement, and a FontCollection object.
helpviewer_keywords: ["Font","Font class [GDI+]","Font constructor","Font constructor [GDI+]","Font constructor [GDI+]","Font class","Font.Font","Font.Font(IN const WCHAR","IN REAL","IN INT","IN Unit","IN const FontCollection)","Font.Font(const WCHAR*","REAL","INT","Unit","const FontCollection*)","Font::Font","Font::Font(IN const WCHAR","IN REAL","IN INT","IN Unit","IN const FontCollection)","_gdiplus_CLASS_Font_Font_familyName_emSize_style_unit_fontCollection_","gdiplus._gdiplus_CLASS_Font_Font_familyName_emSize_style_unit_fontCollection_"]
old-location: gdiplus\_gdiplus_CLASS_Font_Font_familyName_emSize_style_unit_fontCollection_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\fontclass\fontconstructors\font_74familyname_emsize_style_unit_fontcolle.htm
ms.date: 12/05/2018
ms.keywords: Font, Font class [GDI+],Font constructor, Font constructor [GDI+], Font constructor [GDI+],Font class, Font.Font, Font.Font(IN const WCHAR,IN REAL,IN INT,IN Unit,IN const FontCollection), Font.Font(const WCHAR*,REAL,INT,Unit,const FontCollection*), Font::Font, Font::Font(IN const WCHAR,IN REAL,IN INT,IN Unit,IN const FontCollection), _gdiplus_CLASS_Font_Font_familyName_emSize_style_unit_fontCollection_, gdiplus._gdiplus_CLASS_Font_Font_familyName_emSize_style_unit_fontCollection_
f1_keywords:
- gdiplusheaders/Font.Font
dev_langs:
- c++
req.header: gdiplusheaders.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
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
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Gdiplus.dll
api_name:
- Font.Font
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# Font::Font(IN const WCHAR,IN REAL,IN INT,IN Unit,IN const FontCollection)


## -description


Creates a <b>Font::Font</b> object based on a font family, a size, a font style, a unit of measurement, and a 
			<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontcollection">FontCollection</a> object.


## -parameters




### -param familyName [in]

Type: <b>const WCHAR*</b>

Name of the font family. 


### -param emSize [in]

Type: <b>REAL</b>

Real number that specifies the em size of the font measured in the units specified in the 
					<i>unit</i> parameter. 


### -param style [in]

Type: <b>INT</b>

Optional. Integer that specifies the style of the typeface. This value must be an element of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-fontstyle">FontStyle</a> enumeration or the result of a bitwise 
					<b>OR</b> applied to two or more of these elements. For example, <code>FontStyleBold</code> | <code>FontStyleUnderline</code> | <code>FontStyleStrikeout</code>  sets the style as a combination of the three styles. The default value is <code>FontStyleRegular</code>. 


### -param unit [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-unit">Unit</a></b>

Optional. Element of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-unit">Unit</a> enumeration that specifies the unit of measurement for the font size. The default value is <code>UnitPoint</code>. 


### -param fontCollection [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontcollection">FontCollection</a>*</b>

Optional. Pointer to a 
					<b>FontCollection</b> object that specifies a user-defined group of fonts. If the value of this parameter is <b>NULL</b>, the system font collection is used. The default value is <b>NULL</b>. 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font">Font</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily">FontFamily</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-fontstyle">FontStyle</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-unit">Unit</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-using-text-and-fonts-use">Using Text and Fonts</a>
 

 


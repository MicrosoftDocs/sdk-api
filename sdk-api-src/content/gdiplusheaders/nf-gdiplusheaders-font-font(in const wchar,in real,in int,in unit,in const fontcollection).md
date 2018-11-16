---
UID: NF:gdiplusheaders.Font.Font(IN const WCHAR,IN REAL,IN INT,IN Unit,IN const FontCollection)
title: Font::Font(IN const WCHAR,IN REAL,IN INT,IN Unit,IN const FontCollection)
author: windows-sdk-content
description: Creates a Font::Font object based on a font family, a size, a font style, a unit of measurement, and a FontCollection object.
old-location: gdiplus\_gdiplus_CLASS_Font_Font_familyName_emSize_style_unit_fontCollection_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\fontclass\fontconstructors\font_74familyname_emsize_style_unit_fontcolle.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Font, Font class [GDI+],Font constructor, Font constructor [GDI+], Font constructor [GDI+],Font class, Font.Font, Font.Font(IN const WCHAR,IN REAL,IN INT,IN Unit,IN const FontCollection), Font.Font(const WCHAR*,REAL,INT,Unit,const FontCollection*), Font::Font, Font::Font(IN const WCHAR,IN REAL,IN INT,IN Unit,IN const FontCollection), _gdiplus_CLASS_Font_Font_familyName_emSize_style_unit_fontCollection_, gdiplus._gdiplus_CLASS_Font_Font_familyName_emSize_style_unit_fontCollection_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- gdiplusheaders.h
: 
- Font.Font
: 
req.product: GDI+ 1.0
---

# Font::Font(IN const WCHAR,IN REAL,IN INT,IN Unit,IN const FontCollection)


## -description


Creates a <b>Font::Font</b> object based on a font family, a size, a font style, a unit of measurement, and a 
			<a href="https://msdn.microsoft.com/en-us/library/ms534438(v=VS.85).aspx">FontCollection</a> object.


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

Optional. Integer that specifies the style of the typeface. This value must be an element of the <a href="https://msdn.microsoft.com/de08c779-1f43-4740-b2b9-8d3906dc4432">FontStyle</a> enumeration or the result of a bitwise 
					<b>OR</b> applied to two or more of these elements. For example, <code>FontStyleBold</code> | <code>FontStyleUnderline</code> | <code>FontStyleStrikeout</code>  sets the style as a combination of the three styles. The default value is <code>FontStyleRegular</code>. 


### -param unit [in]

Type: <b><a href="https://msdn.microsoft.com/33f0b0fd-7764-48bc-874e-26cc522d5362">Unit</a></b>

Optional. Element of the <a href="https://msdn.microsoft.com/33f0b0fd-7764-48bc-874e-26cc522d5362">Unit</a> enumeration that specifies the unit of measurement for the font size. The default value is <code>UnitPoint</code>. 


### -param fontCollection [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534438(v=VS.85).aspx">FontCollection</a>*</b>

Optional. Pointer to a 
					<b>FontCollection</b> object that specifies a user-defined group of fonts. If the value of this parameter is <b>NULL</b>, the system font collection is used. The default value is <b>NULL</b>. 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534437(v=VS.85).aspx">Font</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534439(v=VS.85).aspx">FontFamily</a>



<a href="https://msdn.microsoft.com/de08c779-1f43-4740-b2b9-8d3906dc4432">FontStyle</a>



<a href="https://msdn.microsoft.com/33f0b0fd-7764-48bc-874e-26cc522d5362">Unit</a>



<a href="https://msdn.microsoft.com/12bc38c3-5fbc-4d7b-902c-92a5f5057473">Using Text and Fonts</a>
 

 


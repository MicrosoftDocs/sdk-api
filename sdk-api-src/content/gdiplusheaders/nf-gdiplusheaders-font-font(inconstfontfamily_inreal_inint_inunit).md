---
UID: NF:gdiplusheaders.Font.Font(IN const FontFamily,IN REAL,IN INT,IN Unit)
title: Font::Font(IN const FontFamily,IN REAL,IN INT,IN Unit) (gdiplusheaders.h)
author: windows-sdk-content
description: Creates a Font::Font object based on a FontFamily object, a size, a font style, and a unit of measurement.
old-location: gdiplus\_gdiplus_CLASS_Font_Font_family_emSize_style_unit_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\fontclass\fontconstructors\font_0family_emsize_style_unit.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Font, Font class [GDI+],Font constructor, Font constructor [GDI+], Font constructor [GDI+],Font class, Font.Font, Font.Font(IN const FontFamily,IN REAL,IN INT,IN Unit), Font.Font(const FontFamily*,REAL,INT,Unit), Font::Font, Font::Font(IN const FontFamily,IN REAL,IN INT,IN Unit), _gdiplus_CLASS_Font_Font_family_emSize_style_unit_, gdiplus._gdiplus_CLASS_Font_Font_family_emSize_style_unit_
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
req.product: GDI+ 1.0
---

# Font::Font(IN const FontFamily,IN REAL,IN INT,IN Unit)


## -description


Creates a <b>Font::Font</b> object based on a <a href="https://msdn.microsoft.com/en-us/library/ms534439(v=VS.85).aspx">FontFamily</a> object, a size, a font style, and a unit of measurement.


## -parameters




### -param family [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534439(v=VS.85).aspx">FontFamily</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms534439(v=VS.85).aspx">FontFamily</a> object that specifies information such as the string that identifies the font family and the font family's text metrics measured in design units. 


### -param emSize [in]

Type: <b>REAL</b>

Real number that specifies the em size of the font measured in the units specified in the 
					<i>unit</i> parameter. 


### -param style [in]

Type: <b>INT</b>

Optional. Integer that specifies the style of the typeface. This value must be an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534124(v=VS.85).aspx">FontStyle</a> enumeration or the result of a bitwise 
					<b>OR</b> applied to two or more of these elements. For example, FontStyleBold | FontStyleUnderline | FontStyleStrikeout  sets the style as a combination of the three styles. The default value is FontStyleRegular. 


### -param unit [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534405(v=VS.85).aspx">Unit</a></b>

Optional. Element of the <a href="https://msdn.microsoft.com/en-us/library/ms534405(v=VS.85).aspx">Unit</a> enumeration that specifies the unit of measurement for the font size. The default value is UnitPoint. 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534437(v=VS.85).aspx">Font</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534439(v=VS.85).aspx">FontFamily</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534124(v=VS.85).aspx">FontStyle</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534405(v=VS.85).aspx">Unit</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533817(v=VS.85).aspx">Using Text and Fonts</a>
 

 


---
UID: NF:gdiplusgraphics.Graphics.MeasureDriverString
title: Graphics::MeasureDriverString
author: windows-sdk-content
description: The Graphics::MeasureDriverString method measures the bounding box for the specified characters and their corresponding positions.
old-location: gdiplus\_gdiplus_CLASS_Graphics_MeasureDriverString_text_length_font_positions_flags_matrix_boundingBox_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\measuredriverstring.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: Graphics class [GDI+],MeasureDriverString method, Graphics.MeasureDriverString, Graphics::MeasureDriverString, MeasureDriverString, MeasureDriverString method [GDI+], MeasureDriverString method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_MeasureDriverString_text_length_font_positions_flags_matrix_boundingBox_, gdiplus._gdiplus_CLASS_Graphics_MeasureDriverString_text_length_font_positions_flags_matrix_boundingBox_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: gdiplusgraphics.h
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Graphics.MeasureDriverString
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Graphics::MeasureDriverString


## -description


The <b>Graphics::MeasureDriverString</b> method measures the bounding box for the specified characters and their corresponding positions.


## -parameters




### -param text [in]

Type: <b>const UINT16*</b>

Pointer to an array of 16-bit values. If the DriverStringOptionsCmapLookup flag is set, each value specifies a Unicode character to be displayed. Otherwise, each value specifies an index to a font glyph that defines a character to be displayed. 


### -param length [in]

Type: <b>INT</b>

Integer that specifies the number of values in the <i>text</i> array. The <i>length</i> parameter can be set to –1 if the string is null terminated. 


### -param font [in]

Type: <b>const <a href="https://msdn.microsoft.com/library/ms534437(v=VS.85).aspx">Font</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/library/ms534437(v=VS.85).aspx">Font</a> object that specifies the family name, size, and style of the font to be applied to the string. 


### -param positions [in]

Type: <b>const <a href="https://msdn.microsoft.com/library/ms534488(v=VS.85).aspx">PointF</a>*</b>

If the DriverStringOptionsRealizedAdvance flag is set, <i>positions</i> is a pointer to a <a href="https://msdn.microsoft.com/library/ms534488(v=VS.85).aspx">PointF</a> object that specifies the position of the first glyph. Otherwise, <i>positions</i> is an array of <b>PointF</b> objects, each of which specifies the origin of an individual glyph. 


### -param flags [in]

Type: <b>INT</b>

Integer that specifies the options for the appearance of the string. This value must be an element of the <a href="https://msdn.microsoft.com/library/ms534108(v=VS.85).aspx">DriverStringOptions</a> enumeration or the result of a bitwise <b>OR</b> applied to two or more of these elements. 


### -param matrix [in]

Type: <b>const <a href="https://msdn.microsoft.com/library/ms534475(v=VS.85).aspx">Matrix</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/library/ms534475(v=VS.85).aspx">Matrix</a> object that specifies the transformation matrix to apply to each value in the <i>text</i> array. 


### -param boundingBox [out]

Type: <b><a href="https://msdn.microsoft.com/library/ms534497(v=VS.85).aspx">RectF</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/library/ms534497(v=VS.85).aspx">RectF</a> object that receives the rectangle that bounds the string. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/library/ms534108(v=VS.85).aspx">DriverStringOptions</a>



<a href="https://msdn.microsoft.com/library/ms534437(v=VS.85).aspx">Font</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a>



<a href="https://msdn.microsoft.com/library/ms535683(v=VS.85).aspx">Graphics::DrawDriverString</a>



<a href="https://msdn.microsoft.com/library/ms534475(v=VS.85).aspx">Matrix</a>



<a href="https://msdn.microsoft.com/library/ms534497(v=VS.85).aspx">RectF</a>



<a href="https://msdn.microsoft.com/library/ms534508(v=VS.85).aspx">SolidBrush</a>
 

 


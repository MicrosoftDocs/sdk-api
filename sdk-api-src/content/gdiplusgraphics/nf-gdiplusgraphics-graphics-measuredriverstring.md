---
UID: NF:gdiplusgraphics.Graphics.MeasureDriverString
title: Graphics::MeasureDriverString
author: windows-sdk-content
description: The Graphics::MeasureDriverString method measures the bounding box for the specified characters and their corresponding positions.
old-location: gdiplus\_gdiplus_CLASS_Graphics_MeasureDriverString_text_length_font_positions_flags_matrix_boundingBox_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\measuredriverstring.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Graphics class [GDI+],MeasureDriverString method, Graphics.MeasureDriverString, Graphics::MeasureDriverString, MeasureDriverString, MeasureDriverString method [GDI+], MeasureDriverString method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_MeasureDriverString_text_length_font_positions_flags_matrix_boundingBox_, gdiplus._gdiplus_CLASS_Graphics_MeasureDriverString_text_length_font_positions_flags_matrix_boundingBox_
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - Graphics.MeasureDriverString
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

Type: <b>const <a href="https://msdn.microsoft.com/dd8af524-688c-44dd-b3e4-deadb874bdc3">Font</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/dd8af524-688c-44dd-b3e4-deadb874bdc3">Font</a> object that specifies the family name, size, and style of the font to be applied to the string. 


### -param positions [in]

Type: <b>const <a href="https://msdn.microsoft.com/2d357844-19a8-4ada-ba1e-685fea2e65ce">PointF</a>*</b>

If the DriverStringOptionsRealizedAdvance flag is set, <i>positions</i> is a pointer to a <a href="https://msdn.microsoft.com/2d357844-19a8-4ada-ba1e-685fea2e65ce">PointF</a> object that specifies the position of the first glyph. Otherwise, <i>positions</i> is an array of <b>PointF</b> objects, each of which specifies the origin of an individual glyph. 


### -param flags [in]

Type: <b>INT</b>

Integer that specifies the options for the appearance of the string. This value must be an element of the <a href="https://msdn.microsoft.com/5cf327d5-5ffa-4f10-994a-2e5153b36dd7">DriverStringOptions</a> enumeration or the result of a bitwise <b>OR</b> applied to two or more of these elements. 


### -param matrix [in]

Type: <b>const <a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a> object that specifies the transformation matrix to apply to each value in the <i>text</i> array. 


### -param boundingBox [out]

Type: <b><a href="https://msdn.microsoft.com/6821442b-d352-48cb-a48a-839105a8c36a">RectF</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/6821442b-d352-48cb-a48a-839105a8c36a">RectF</a> object that receives the rectangle that bounds the string. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/5cf327d5-5ffa-4f10-994a-2e5153b36dd7">DriverStringOptions</a>



<a href="https://msdn.microsoft.com/dd8af524-688c-44dd-b3e4-deadb874bdc3">Font</a>



<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>



<a href="https://msdn.microsoft.com/daed7b4e-5284-4a38-bd33-274618f01027">Graphics::DrawDriverString</a>



<a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>



<a href="https://msdn.microsoft.com/6821442b-d352-48cb-a48a-839105a8c36a">RectF</a>



<a href="https://msdn.microsoft.com/8d5c8780-f03c-40b2-b237-e40121e3d6f6">SolidBrush</a>
 

 


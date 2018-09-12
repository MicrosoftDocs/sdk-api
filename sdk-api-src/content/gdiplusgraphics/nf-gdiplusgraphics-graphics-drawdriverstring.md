---
UID: NF:gdiplusgraphics.Graphics.DrawDriverString
title: Graphics::DrawDriverString
author: windows-sdk-content
description: The Graphics::DrawDriverString method draws characters at the specified positions. The method gives the client complete control over the appearance of text. The method assumes that the client has already set up the format and layout to be applied.
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawDriverString_text_length_font_brush_positions_flags_matrix_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\drawdriverstring.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: DrawDriverString, DrawDriverString method [GDI+], DrawDriverString method [GDI+],Graphics class, Graphics class [GDI+],DrawDriverString method, Graphics.DrawDriverString, Graphics::DrawDriverString, _gdiplus_CLASS_Graphics_DrawDriverString_text_length_font_brush_positions_flags_matrix_, gdiplus._gdiplus_CLASS_Graphics_DrawDriverString_text_length_font_brush_positions_flags_matrix_
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
 - Graphics.DrawDriverString
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Graphics::DrawDriverString


## -description


The <b>Graphics::DrawDriverString</b> method draws characters at the specified positions. The method gives the client complete control over the appearance of text. The method assumes that the client has already set up the format and layout to be applied.


## -parameters




### -param text [in]

Type: <b>const UINT16*</b>

Pointer to an array of 16-bit values. If the <b>DriverStringOptionsCmapLookup</b> flag is set, each value specifies a Unicode character to be displayed. Otherwise, each value specifies an index to a font glyph that defines a character to be displayed. 


### -param length [in]

Type: <b>INT</b>

Integer that specifies the number of values in the 
					<i>text</i> array. The 
					<i>length</i> parameter can be set to 
					–1 if the string is null terminated. 


### -param font [in]

Type: <b>const <a href="https://msdn.microsoft.com/dd8af524-688c-44dd-b3e4-deadb874bdc3">Font</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/dd8af524-688c-44dd-b3e4-deadb874bdc3">Font</a> object that specifies the family name, size, and style of the font that is to be applied to the string. 


### -param brush [in]

Type: <b>const <a href="https://msdn.microsoft.com/37cfc0f8-8e17-4944-85fc-cc80ebff13df">Brush</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/37cfc0f8-8e17-4944-85fc-cc80ebff13df">Brush</a> object that is used to fill the string. 


### -param positions [in]

Type: <b>const <a href="https://msdn.microsoft.com/2d357844-19a8-4ada-ba1e-685fea2e65ce">PointF</a>*</b>

If the DriverStringOptionsRealizedAdvance flag is set, <i>positions</i> is a pointer to a <a href="https://msdn.microsoft.com/2d357844-19a8-4ada-ba1e-685fea2e65ce">PointF</a> object that specifies the position of the first glyph. Otherwise, <i>positions</i> is an array of <b>PointF</b> objects, each of which specifies the origin of an individual glyph. 


### -param flags [in]

Type: <b>INT</b>

Integer that specifies the options for the appearance of the string. This value must be an element of the <a href="https://msdn.microsoft.com/5cf327d5-5ffa-4f10-994a-2e5153b36dd7">DriverStringOptions</a> enumeration or the result of a bitwise 
					<b>OR</b> applied to two or more of these elements. 


### -param matrix [in]

Type: <b>const <a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a> object that specifies the transformation matrix to apply to each value in the 
					<i>text</i> array. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



This method does not support the handling of complex scripts and assumes that the client has set up all text layout in some other way. This method is useful for creating owner-drawn menu items. The client should use the 
				<a href="https://msdn.microsoft.com/b3568ed9-e359-4916-a83d-7553c021d197">DrawString Methods</a> method for general purposes.




## -see-also




<a href="https://msdn.microsoft.com/37cfc0f8-8e17-4944-85fc-cc80ebff13df">Brush</a>



<a href="https://msdn.microsoft.com/b3568ed9-e359-4916-a83d-7553c021d197">DrawString Methods</a>



<a href="https://msdn.microsoft.com/5cf327d5-5ffa-4f10-994a-2e5153b36dd7">DriverStringOptions</a>



<a href="https://msdn.microsoft.com/dd8af524-688c-44dd-b3e4-deadb874bdc3">Font</a>



<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>



<a href="https://msdn.microsoft.com/f68ee34e-84e9-4af1-b5f7-018b875d80ad">Graphics::MeasureDriverString</a>



<a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>



<a href="https://msdn.microsoft.com/2d357844-19a8-4ada-ba1e-685fea2e65ce">PointF</a>
 

 


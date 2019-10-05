---
UID: NF:gdiplusgraphics.Graphics.DrawString(const WCHAR,INT,const Font,const PointF &,const Brush)
title: Graphics::DrawString(const WCHAR,INT,const Font,const PointF &,const Brush) (gdiplusgraphics.h)
author: windows-sdk-content
description: The Graphics::DrawString method draws a string based on a font and an origin for the string.
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawString_string_length_font_origin_brush_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsdrawstringmethods\drawstring_75string_length_font_origin_brush.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DrawString, DrawString method [GDI+], DrawString method [GDI+],Graphics class, Graphics class [GDI+],DrawString method, Graphics.DrawString, Graphics.DrawString(const WCHAR*,INT,const Font*,const PointF&,const Brush*), Graphics.DrawString(const WCHAR,INT,const Font,const PointF &,const Brush), Graphics::DrawString, Graphics::DrawString(const WCHAR,INT,const Font,const PointF &,const Brush), _gdiplus_CLASS_Graphics_DrawString_string_length_font_origin_brush_, gdiplus._gdiplus_CLASS_Graphics_DrawString_string_length_font_origin_brush_
ms.topic: method
f1_keywords: 
 - "gdiplusgraphics/Graphics.DrawString"
dev_langs:
 - c++
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
 - Graphics.DrawString
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# Graphics::DrawString(const WCHAR,INT,const Font,const PointF &,const Brush)


## -description


The <b>Graphics::DrawString</b> method draws a string based on a font and an origin for the string.


## -parameters




### -param string [in]

Type: <b>const WCHAR*</b>

Pointer to a wide-character string to be drawn. 


### -param length [in]

Type: <b>INT</b>

Integer that specifies the number of characters in the 
					<i>string</i> array. The 
					<i>length</i> parameter can be set to 
					–1 if the string is null terminated. 


### -param font [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font">Font</a>*</b>

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font">Font</a> object that specifies the font attributes (the family name, the size, and the style of the font) to use. 


### -param origin [in, ref]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a></b>

Reference to a 
					<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a> object that specifies the starting point for the string. 


### -param brush [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush">Brush</a>*</b>

Pointer to a 
					<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush">Brush</a> object that is used to fill the string. 


## -returns



Type: <strong>Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.




## -remarks



Note that GDI+ does not support PostScript fonts or OpenType fonts which do not have TrueType outlines. 

When you use the GDI+ API, you must not allow your application to download arbitrary fonts from untrusted sources. 
The operating system requires elevated privileges to assure that all installed fonts are trusted. 



#### Examples



The following example draws a string at the specified origin.


```cpp
VOID Example_DrawString2(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a string.
   WCHAR string[] = L"Sample Text";

   // Initialize arguments.
   Font myFont(L"Arial", 16);
   PointF origin(0.0f, 0.0f);
   SolidBrush blackBrush(Color(255, 0, 0, 0));

   // Draw string.
   graphics.DrawString(
   string,
   11,
   &myFont,
   origin,
   &blackBrush);
}
```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font">Font</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush">SolidBrush</a>
 

 


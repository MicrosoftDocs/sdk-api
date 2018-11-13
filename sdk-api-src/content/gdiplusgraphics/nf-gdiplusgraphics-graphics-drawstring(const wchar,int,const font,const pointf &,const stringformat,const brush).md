---
UID: NF:gdiplusgraphics.Graphics.DrawString(const WCHAR,INT,const Font,const PointF &,const StringFormat,const Brush)
title: Graphics::DrawString(const WCHAR,INT,const Font,const PointF &,const StringFormat,const Brush)
author: windows-sdk-content
description: The Graphics::DrawString method draws a string based on a font, a string origin, and a format.
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawString_string_length_font_origin_stringFormat_brush_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsdrawstringmethods\drawstring_83string_length_font_origin_stringformat.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: DrawString, DrawString method [GDI+], DrawString method [GDI+],Graphics class, Graphics class [GDI+],DrawString method, Graphics.DrawString, Graphics.DrawString(const WCHAR*,INT,const Font*,const PointF&,const StringFormat*,const Brush*), Graphics.DrawString(const WCHAR,INT,const Font,const PointF &,const StringFormat,const Brush), Graphics::DrawString, Graphics::DrawString(const WCHAR,INT,const Font,const PointF &,const StringFormat,const Brush), _gdiplus_CLASS_Graphics_DrawString_string_length_font_origin_stringFormat_brush_, gdiplus._gdiplus_CLASS_Graphics_DrawString_string_length_font_origin_stringFormat_brush_
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
 - Graphics.DrawString
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Graphics::DrawString(const WCHAR,INT,const Font,const PointF &,const StringFormat,const Brush)


## -description


The <b>Graphics::DrawString</b> method draws a string based on a font, a string origin, and a format.


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

Type: <b>const <a href="https://msdn.microsoft.com/dd8af524-688c-44dd-b3e4-deadb874bdc3">Font</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/dd8af524-688c-44dd-b3e4-deadb874bdc3">Font</a> object that specifies the font attributes (the family name, the size, and the style of the font) to use. 


### -param origin [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/2d357844-19a8-4ada-ba1e-685fea2e65ce">PointF</a></b>

Reference to a <a href="https://msdn.microsoft.com/2d357844-19a8-4ada-ba1e-685fea2e65ce">PointF</a> object that specifies the starting point for the string. 


### -param stringFormat [in]

Type: <b>const <a href="https://msdn.microsoft.com/2d7af5fe-f3e9-4db3-90a5-4e623d9ce773">StringFormat</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/2d7af5fe-f3e9-4db3-90a5-4e623d9ce773">StringFormat</a> object that specifies text layout information and display manipulations to be applied to the string. 


### -param brush [in]

Type: <b>const <a href="https://msdn.microsoft.com/37cfc0f8-8e17-4944-85fc-cc80ebff13df">Brush</a>*</b>

Pointer to a 
					<a href="https://msdn.microsoft.com/37cfc0f8-8e17-4944-85fc-cc80ebff13df">Brush</a> object that is used to fill the string. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



Note that GDI+ does not support PostScript fonts or OpenType fonts which do not have TrueType outlines. 

When you use the GDI+ API, you must not allow your application to download arbitrary fonts from untrusted sources. 
The operating system requires elevated privileges to assure that all installed fonts are trusted. 



#### Examples



The following example uses the specified formatting to draw a string at the specified origin.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_DrawString3(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a string.
   WCHAR string[] = L"Sample Text";
   
   // Initialize arguments.
   Font myFont(L"Arial", 16);
   PointF origin(0.0f, 0.0f);
   SolidBrush blackBrush(Color(255, 0, 0, 0));
   StringFormat format;
   format.SetAlignment(StringAlignmentCenter);

   // Draw string.
   graphics.DrawString(
   string,
   11,
   &amp;myFont,
   origin,
   &amp;format,
   &amp;blackBrush);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/dd8af524-688c-44dd-b3e4-deadb874bdc3">Font</a>



<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>



<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a>



<a href="https://msdn.microsoft.com/2d357844-19a8-4ada-ba1e-685fea2e65ce">PointF</a>



<a href="https://msdn.microsoft.com/2d7af5fe-f3e9-4db3-90a5-4e623d9ce773">StringFormat</a>
 

 


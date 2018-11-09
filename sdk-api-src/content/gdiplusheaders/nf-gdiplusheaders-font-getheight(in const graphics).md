---
UID: NF:gdiplusheaders.Font.GetHeight(IN const Graphics)
title: Font::GetHeight(IN const Graphics)
author: windows-sdk-content
description: The Font::GetHeight method gets the line spacing of this font in the current unit of a specified Graphics object.
old-location: gdiplus\_gdiplus_CLASS_Font_GetHeight_graphics_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\fontclass\fontmethods\fontgetheightmethods\getheight_62graphics.htm
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: Font class [GDI+],GetHeight method, Font.GetHeight, Font.GetHeight(IN const Graphics), Font.GetHeight(const Graphics*), Font::GetHeight, Font::GetHeight(IN const Graphics), GetHeight, GetHeight method [GDI+], GetHeight method [GDI+],Font class, _gdiplus_CLASS_Font_GetHeight_graphics_, gdiplus._gdiplus_CLASS_Font_GetHeight_graphics_
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
 - Font.GetHeight
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Font::GetHeight(IN const Graphics)


## -description


The <b>Font::GetHeight</b> method gets the line spacing of this font in the current unit of a specified <a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object. The line spacing is the vertical distance between the base lines of two consecutive lines of text. Thus, the line spacing includes the blank space between lines along with the height of the character itself.


## -parameters




### -param graphics [in]

Type: <b>const Graphics*</b>

Pointer to a <a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object whose unit and vertical resolution are used in the height calculation. 


## -returns



Type: <strong>Type: <b>REAL</b>
</strong>

This method returns the line spacing of this font.




## -remarks



If the font unit is set to anything other than <a href="https://msdn.microsoft.com/33f0b0fd-7764-48bc-874e-26cc522d5362">UnitPixel</a>, the height, in pixels, is calculated using the vertical resolution of the specified <a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object. For example, suppose the font unit is inches and the font size is 0.3. Also suppose that for the corresponding font family, the em height is 2048 and the line spacing is 2355. If the unit of the <b>Graphics</b> object is <a href="https://msdn.microsoft.com/33f0b0fd-7764-48bc-874e-26cc522d5362">UnitPixel</a> and the vertical resolution of the <b>Graphics</b> object is 96 dots per inch, the height is calculated as follows:

2355*(0.3/2048)*96 = 33.1171875

Continuing with the same example, suppose the unit of the <a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object is something other than <a href="https://msdn.microsoft.com/33f0b0fd-7764-48bc-874e-26cc522d5362">UnitPixel</a>, say <a href="https://msdn.microsoft.com/33f0b0fd-7764-48bc-874e-26cc522d5362">UnitMillimeter</a>. Then (using 1 inch = 25.4 millimeters) the height, in millimeters, is calculated as follows:

2355*(0.3/2048)25.4 = 8.762256


#### Examples



The following example creates a 
						<a href="https://msdn.microsoft.com/dd8af524-688c-44dd-b3e4-deadb874bdc3">Font</a> object, retrieves the height of the 
						<b>Font</b> object, and uses the height to position two lines of text, with the second line directly below the first.


```cpp
VOID Example_GetHeight(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a Font object.
   Font myFont(L"Arial", 16);

   // Draw text with myFont.
   SolidBrush solidbrush_1(Color(255, 0, 0, 0));
   WCHAR string[] = L"The first line of text";
   graphics.DrawString(string, 22, &myFont, PointF(0, 0), &solidbrush_1);

   // Get the height of myFont.
   REAL height = myFont.GetHeight(&graphics);

   // Draw text immediately below the first line of text.
   SolidBrush solidbrush_2(Color(255, 255, 0, 0));
   WCHAR string[] = L"The second line of text";
   graphics.DrawString(string2, 23, &myFont, PointF(0, height),
                       &solidbrush_2);
}
```





## -see-also




<a href="https://msdn.microsoft.com/dd8af524-688c-44dd-b3e4-deadb874bdc3">Font</a>



<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>



<a href="https://msdn.microsoft.com/12bc38c3-5fbc-4d7b-902c-92a5f5057473">Using Text and Fonts</a>
 

 


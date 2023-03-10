---
UID: NF:gdiplusgraphics.Graphics.MeasureCharacterRanges
title: Graphics::MeasureCharacterRanges (gdiplusgraphics.h)
description: The Graphics::MeasureCharacterRanges method gets a set of regions each of which bounds a range of character positions within a string.
helpviewer_keywords: ["Graphics class [GDI+]","MeasureCharacterRanges method","Graphics.MeasureCharacterRanges","Graphics::MeasureCharacterRanges","MeasureCharacterRanges","MeasureCharacterRanges method [GDI+]","MeasureCharacterRanges method [GDI+]","Graphics class","_gdiplus_CLASS_Graphics_MeasureCharacterRanges_string_length_font_layoutRect_stringFormat_regionCoun","gdiplus._gdiplus_CLASS_Graphics_MeasureCharacterRanges_string_length_font_layoutRect_stringFormat_regionCoun"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_MeasureCharacterRanges_string_length_font_layoutRect_stringFormat_regionCoun.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\measurecharacterranges.htm
ms.date: 12/05/2018
ms.keywords: Graphics class [GDI+],MeasureCharacterRanges method, Graphics.MeasureCharacterRanges, Graphics::MeasureCharacterRanges, MeasureCharacterRanges, MeasureCharacterRanges method [GDI+], MeasureCharacterRanges method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_MeasureCharacterRanges_string_length_font_layoutRect_stringFormat_regionCoun, gdiplus._gdiplus_CLASS_Graphics_MeasureCharacterRanges_string_length_font_layoutRect_stringFormat_regionCoun
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - Graphics::MeasureCharacterRanges
 - gdiplusgraphics/Graphics::MeasureCharacterRanges
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Graphics.MeasureCharacterRanges
---

# Graphics::MeasureCharacterRanges


## -description

The <b>Graphics::MeasureCharacterRanges</b> method gets a set of regions each of which bounds a range of character positions within a string.

## -parameters

### -param string [in]

Type: <b>const WCHAR*</b>

Pointer to a wide-character string. 

<div class="alert"><b>Important</b>  For bidirectional languages, such as Arabic, the string length must not exceed 2046 characters.</div>
<div> </div>

### -param length [in]

Type: <b>INT</b>

Integer that specifies the number of characters in the <i>string</i> array. If the <i>string</i> parameter points to a <b>NULL</b>-terminated string, this parameter can be set to –1.

### -param font [in]

Type: <b>const <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font">Font</a>*</b>

Pointer to a <i>Font</i> object that specifies the font characteristics (the family name, size, and style of the font) to be applied to the string.

### -param layoutRect [in, ref]

Type: <b>const Rectf</b>

Reference to a rectangle that bounds the string.

### -param stringFormat [in]

Type: <b>const <a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a>*</b>

Pointer to a <i>StringFormat</i> object that specifies the character ranges and layout information, such as alignment, trimming, tab stops, and so forth.

### -param regionCount [in]

Type: <b>INT</b>

Integer that specifies the number of regions that are expected to be received into the <i>regions</i> array. This number should be equal to the number of character ranges currently in the <i>StringFormat</i> object.

### -param regions [out]

Type: <b><a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region">Region</a>*</b>

Pointer to an array of <i>Region</i> objects that receives the regions, each of which bounds a range of text.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

A character range is a range of character positions within a string of text. The area of the display that is occupied by a group of characters that are specified by the character range, is the bounding region. A character range is set by <a href="/windows/desktop/api/gdiplusstringformat/nf-gdiplusstringformat-stringformat-setmeasurablecharacterranges">SetMeasurableCharacterRanges</a>. The number of ranges that are currently set can be determined by calling <a href="/windows/desktop/api/gdiplusstringformat/nf-gdiplusstringformat-stringformat-getmeasurablecharacterrangecount">GetMeasurableCharacterRangeCount</a>. This number is also the number of regions expected to be obtained by the <b>MeasureCharacterRanges</b> method.


#### Examples



The following example defines three ranges of character positions within a string and sets those ranges in a <i>StringFormat</i> object. Next, the <b>MeasureCharacterRanges</b> method is used to get the three regions of the display that are occupied by the characters that are specified by the ranges. This is done for three different layout rectangles to show how the regions change according to the layout of the string. Also, on the third repetition of this, the string format flags are changed so that the regions measured will include trailing spaces.


```cpp
VOID MeasureCharRanges(HDC hdc)
{
   Graphics graphics(hdc);

   // Brushes and pens used for drawing and painting
   SolidBrush blueBrush(Color(255, 0, 0, 255));
   SolidBrush redBrush(Color(100, 255, 0, 0));
   Pen        blackPen(Color(255, 0, 0, 0));

   // Layout rectangles used for drawing strings
   RectF   layoutRect_A(20.0f, 20.0f, 130.0f, 130.0f);
   RectF   layoutRect_B(160.0f, 20.0f, 165.0f, 130.0f);
   RectF   layoutRect_C(335.0f, 20.0f, 165.0f, 130.0f);

   // Three different ranges of character positions within the string
   CharacterRange charRanges[3] = { CharacterRange(3, 5),
                                    CharacterRange(15, 2),
                                    CharacterRange(30, 15), };

   // Font and string format to apply to string when drawing
   Font         myFont(L"Times New Roman", 16.0f);
   StringFormat strFormat;

    // Other variables
   Region* pCharRangeRegions; // pointer to CharacterRange regions
   short   i;                 // loop counter
   INT     count;             // number of character ranges set
   WCHAR   string[] = L"The quick, brown fox easily jumps over the lazy dog.";


   // Set three ranges of character positions.
   strFormat.SetMeasurableCharacterRanges(3, charRanges);

   // Get the number of ranges that have been set, and allocate memory to 
   // store the regions that correspond to the ranges.
   count = strFormat.GetMeasurableCharacterRangeCount();
   pCharRangeRegions = new Region[count];

   // Get the regions that correspond to the ranges within the string when
   // layout rectangle A is used. Then draw the string, and show the regions.
   graphics.MeasureCharacterRanges(string, -1,
      &myFont, layoutRect_A, &strFormat, count, pCharRangeRegions);
   graphics.DrawString(string, -1,
      &myFont, layoutRect_A, &strFormat, &blueBrush);
   graphics.DrawRectangle(&blackPen, layoutRect_A);
   for ( i = 0; i < count; i++)
   {
      graphics.FillRegion(&redBrush, pCharRangeRegions + i);
   }

   // Get the regions that correspond to the ranges within the string when
   // layout rectangle B is used. Then draw the string, and show the regions.
   graphics.MeasureCharacterRanges(string, -1,
      &myFont, layoutRect_B, &strFormat, count, pCharRangeRegions);
   graphics.DrawString(string, -1,
      &myFont, layoutRect_B, &strFormat, &blueBrush);
   graphics.DrawRectangle(&blackPen, layoutRect_B);
   for ( i = 0; i < count; i++)
   {
      graphics.FillRegion(&redBrush, pCharRangeRegions + i);
   }

   // Get the regions that correspond to the ranges within the string when
   // layout rectangle C is used. Set trailing spaces to be included in the
   // regions. Then draw the string, and show the regions.
   strFormat.SetFormatFlags(StringFormatFlagsMeasureTrailingSpaces);
   graphics.MeasureCharacterRanges(string, -1,
      &myFont, layoutRect_C, &strFormat, count, pCharRangeRegions);
   graphics.DrawString(string, -1,
      &myFont, layoutRect_C, &strFormat, &blueBrush);
   graphics.DrawRectangle(&blackPen, layoutRect_C);
   for ( i = 0; i < count; i++)
   {
      graphics.FillRegion(&redBrush, pCharRangeRegions + i);
   }
   // Delete memory for the range regions.
   delete [] pCharRangeRegions;
}
```

## -see-also

<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-characterrange">CharacterRange</a>



<a href="/windows/desktop/api/gdiplusstringformat/nf-gdiplusstringformat-stringformat-getmeasurablecharacterrangecount">GetMeasurableCharacterRangeCount</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplusstringformat/nf-gdiplusstringformat-stringformat-setmeasurablecharacterranges">SetMeasurableCharacterRanges</a>
---
UID: NF:gdiplusimageattributes.ImageAttributes.GetAdjustedPalette
title: ImageAttributes::GetAdjustedPalette (gdiplusimageattributes.h)
author: windows-sdk-content
description: The ImageAttributes::GetAdjustedPalette method adjusts the colors in a palette according to the adjustment settings of a specified category.
old-location: gdiplus\_gdiplus_CLASS_ImageAttributes_GetAdjustedPalette_colorPalette_colorAdjustType_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageattributesclass\imageattributesmethods\getadjustedpalette.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetAdjustedPalette, GetAdjustedPalette method [GDI+], GetAdjustedPalette method [GDI+],ImageAttributes class, ImageAttributes class [GDI+],GetAdjustedPalette method, ImageAttributes.GetAdjustedPalette, ImageAttributes::GetAdjustedPalette, _gdiplus_CLASS_ImageAttributes_GetAdjustedPalette_colorPalette_colorAdjustType_, gdiplus._gdiplus_CLASS_ImageAttributes_GetAdjustedPalette_colorPalette_colorAdjustType_
ms.topic: method
req.header: gdiplusimageattributes.h
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
 - ImageAttributes.GetAdjustedPalette
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# ImageAttributes::GetAdjustedPalette


## -description


The <b>ImageAttributes::GetAdjustedPalette</b> method adjusts the colors in a palette according to the adjustment settings of a specified category.


## -parameters




### -param colorPalette [in, out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534064(v=VS.85).aspx">ColorPalette</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms534064(v=VS.85).aspx">ColorPalette</a> structure that on input, contains the palette to be adjusted and, on output, receives the adjusted palette. 


### -param colorAdjustType [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534064(v=VS.85).aspx">ColorPalette</a></b>

Element of the <a href="https://msdn.microsoft.com/en-us/library/ms534089(v=VS.85).aspx">ColorAdjustType</a> enumeration that specifies the category whose adjustment settings will be applied to the palette. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Ok</a>, which is an element of the <b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -remarks



An <a href="https://msdn.microsoft.com/en-us/library/ms534464(v=VS.85).aspx">ImageAttributes</a> object maintains color and grayscale settings for five adjustment categories: default, bitmap, brush, pen, and text. For example, you can specify a color-remap table for the default category, a different color-remap table for the bitmap category, and still a different color-remap table for the pen category.

When you call <b>ImageAttributes::GetAdjustedPalette</b>, you can specify the adjustment category that is used to adjust the palette colors. For example, if you pass <a href="https://msdn.microsoft.com/en-us/library/ms534089(v=VS.85).aspx">ColorAdjustTypeBitmap</a> to the <b>ImageAttributes::GetAdjustedPalette</b> method, then the adjustment settings of the bitmap category are used to adjust the palette colors.


#### Examples



The following example initializes a <a href="https://msdn.microsoft.com/en-us/library/ms534064(v=VS.85).aspx">ColorPalette</a> structure with four colors: aqua, black, red, and green. The code also creates an <a href="https://msdn.microsoft.com/en-us/library/ms534464(v=VS.85).aspx">ImageAttributes</a> object and sets its bitmap remap table so that green will be converted to blue. Then the code adjusts the palette colors by passing the address of the palette to the <b>ImageAttributes::GetAdjustedPalette</b> method of the <b>ImageAttributes</b> object. The code displays the four palette colors twice: once before the adjustment and once after the adjustment.


```cpp

VOID Example_GetAdjustedPalette(HDC hdc)
{
   Graphics graphics(hdc);
   INT j;

   // Create a palette that has four entries.
   ColorPalette* palette = 
      (ColorPalette*)malloc(sizeof(ColorPalette) + 3 * sizeof(ARGB));
   palette->Flags = 0;
   palette->Count = 4;

   palette->Entries[0] = 0xFF00FFFF;   // aqua
   palette->Entries[1] = 0xFF000000;   // black
   palette->Entries[2] = 0xFFFF0000;   // red
   palette->Entries[3] = 0xFF00FF00;   // green
  
   // Display the four palette colors with no adjustment.
   SolidBrush brush(Color());
   for(j = 0; j < 4; ++j)
   {
      brush.SetColor(palette->Entries[j]);
      graphics.FillRectangle(&brush, 30*j, 0, 20, 20);
   }

   // Create a remap table that converts green to blue.
   ColorMap map;
      map.oldColor = Color(255, 0, 255, 0);  // green
      map.newColor = Color(255, 0, 0, 255);  // blue

   // Create an ImageAttributes object, and set its bitmap remap table.
   ImageAttributes imAtt;
   imAtt.SetRemapTable(1, &map, ColorAdjustTypeBitmap);

   // Adjust the palette.
   imAtt.GetAdjustedPalette(palette, ColorAdjustTypeBitmap);

   // Display the four palette colors after the adjustment.
   for(j = 0; j < 4; ++j)
   {
      brush.SetColor(palette->Entries[j]);
      graphics.FillRectangle(&brush, 30*j, 30, 20, 20);
   }
}
				
```


The following illustration shows the output of the preceding code. Note that the green in the original palette was changed to blue.

<img alt="Illustration with two rows of colored rectangles; the last of which is green in Row 1, blue in Row 2" src="./images/imageattributesgetadjustedpalette.png"/>

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534420(v=VS.85).aspx">Bitmap</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534427(v=VS.85).aspx">Color</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534089(v=VS.85).aspx">ColorAdjustType</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534062(v=VS.85).aspx">ColorMap</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534064(v=VS.85).aspx">ColorPalette</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534464(v=VS.85).aspx">ImageAttributes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534477(v=VS.85).aspx">Metafile</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534158(v=VS.85).aspx">PaletteFlags</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533809(v=VS.85).aspx">Recoloring</a>
 

 


---
UID: NF:gdipluspath.GraphicsPath.AddString(constWCHAR,INT,constFontFamily,INT,REAL,constPointF&,constStringFormat)
title: GraphicsPath::AddString
description: The GraphicsPath::AddString method adds the outline of a string to this path. (overload 1/3)
tech.root: gdiplus
helpviewer_keywords: ["GraphicsPath::AddString"]
ms.assetid: 1bed1611-addc-464c-a7c9-64810e922a5e
ms.date: 05/13/2019
ms.keywords: GraphicsPath::AddString
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: gdipluspath.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - GraphicsPath::AddString
 - gdipluspath/GraphicsPath::AddString
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdipluspath.h
api_name:
 - GraphicsPath::AddString
---

# GraphicsPath::AddString


## -description

The **GraphicsPath::AddString** method adds the outline of a string to this path.

## -parameters

### -param string

Pointer to a wide-character string.

### -param length

Integer that specifies the number of characters to display.
If the string parameter points to a **NULL**-terminated string, this parameter can be set to –1.

### -param family

Pointer to a **FontFamily** object that specifies the font family for the string.

### -param style

Integer that specifies the style of the typeface.
This value must be an element of the **FontStyle** enumeration or the result of a bitwise **OR** applied to two or more of these elements.
For example, `FontStyleBold | FontStyleUnderline | FontStyleStrikeout` sets the style as a combination of the three styles.

### -param emSize

Real number that specifies the **em** size, in world units, of the string characters.

### -param origin

Reference to a **PointF** object that specifies, in world units, the location of the string.

### -param format

Pointer to a **StringFormat** object that specifies layout information (alignment, trimming, tab stops, and the like) for the string.

## -returns

**Type:** <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

Note that GDI+ does not support PostScript fonts or OpenType fonts which do not have **TrueType** outlines.

#### Examples

The following example creates a <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object path, adds a NULL-terminated string to path, and then draws path.

```cpp
VOID Example_AddString(HDC hdc)
{
   Graphics graphics(hdc);
   FontFamily fontFamily(L"Times New Roman");
   GraphicsPath path;

   path.AddString(
      L"Hello World",
      -1,                 // NULL-terminated string
      &fontFamily,
      FontStyleRegular,
      48, 
      PointF(50.0f, 50.0f),
      NULL);

   Pen pen(Color(255, 255, 0, 0));
   graphics.DrawPath(&pen, &path);
}
```

## -see-also

<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-addstring(inconstwchar_inint_inconstfontfamily_inint_inreal_inconstpoint__inconststringformat)">AddString Methods</a>

<a href="/windows/desktop/gdiplus/-gdiplus-clipping-with-a-region-use">Clipping with a Region</a>

<a href="/windows/desktop/gdiplus/-gdiplus-constructing-and-drawing-paths-use">Constructing and Drawing Paths</a>

<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font">Font</a>

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily">FontFamily</a>

<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-fontstyle">FontStyle</a>

<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>

<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a>

<a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a>

<a href="/windows/desktop/gdiplus/-gdiplus-using-text-and-fonts-use">Using Text and Fonts</a>

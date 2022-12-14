---
UID: NF:gdipluspath.GraphicsPath.AddString(constWCHAR,INT,constFontFamily,INT,REAL,constRectF&,constStringFormat)
title: GraphicsPath::AddString(IN const WCHAR,IN INT,IN const FontFamily,IN INT,IN REAL,IN const RectF &,IN const StringFormat) (gdipluspath.h)
description: The GraphicsPath::AddString method adds the outline of a string to this path. (overload 2/3)
helpviewer_keywords: ["AddString","AddString method [GDI+]","AddString method [GDI+]","GraphicsPath class","GraphicsPath class [GDI+]","AddString method","GraphicsPath.AddString","GraphicsPath.AddString(IN const WCHAR","IN INT","IN const FontFamily","IN INT","IN REAL","IN const RectF &","IN const StringFormat)","GraphicsPath.AddString(const WCHAR*","INT","const FontFamily*","INT","REAL","const RectF&","const StringFormat*)","GraphicsPath::AddString","GraphicsPath::AddString(IN const WCHAR","IN INT","IN const FontFamily","IN INT","IN REAL","IN const RectF &","IN const StringFormat)","_gdiplus_CLASS_GraphicsPath_AddString_wifirr","gdiplus._gdiplus_CLASS_GraphicsPath_AddString_wifirr"]
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_AddString_wifirr.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\graphicspathaddstringmethods\addstring_95wcharstring_intlength_fontfamilyfamily.htm
ms.date: 12/05/2018
ms.keywords: AddString, AddString method [GDI+], AddString method [GDI+],GraphicsPath class, GraphicsPath class [GDI+],AddString method, GraphicsPath.AddString, GraphicsPath.AddString(IN const WCHAR,IN INT,IN const FontFamily,IN INT,IN REAL,IN const RectF &,IN const StringFormat), GraphicsPath.AddString(const WCHAR*,INT,const FontFamily*,INT,REAL,const RectF&,const StringFormat*), GraphicsPath::AddString, GraphicsPath::AddString(IN const WCHAR,IN INT,IN const FontFamily,IN INT,IN REAL,IN const RectF &,IN const StringFormat), _gdiplus_CLASS_GraphicsPath_AddString_wifirr, gdiplus._gdiplus_CLASS_GraphicsPath_AddString_wifirr
req.header: gdipluspath.h
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
 - GraphicsPath::AddString
 - gdipluspath/GraphicsPath::AddString
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
 - GraphicsPath.AddString
---

# GraphicsPath::AddString(IN const WCHAR,IN INT,IN const FontFamily,IN INT,IN REAL,IN const RectF &,IN const StringFormat)


## -description

The <b>GraphicsPath::AddString</b> method adds the outline of a string to this path.

## -parameters

### -param string [in]

Type: <b>const WCHAR*</b>

Pointer to a wide-character string.

### -param length [in]

Type: <b>INT</b>

Integer that specifies the number of characters to display. If the <i>string</i> parameter points to a <b>NULL</b>-terminated string, this parameter can be set to –1.

### -param family [in]

Type: <b>const <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily">FontFamily</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily">FontFamily</a> object that specifies the font family for the string.

### -param style [in]

Type: <b>INT</b>

Integer that specifies the style of the typeface. This value must be an element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-fontstyle">FontStyle</a> enumeration or the result of a bitwise <b>OR</b> applied to two or more of these elements. For example, <code>FontStyleBold | FontStyleUnderline | FontStyleStrikeout</code> sets the style as a combination of the three styles.

### -param emSize [in]

Type: <b>REAL</b>

Real number that specifies the em size, in world units, of the string characters.

### -param layoutRect [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a></b>

Reference to a <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a> object that specifies, in world units, the bounding rectangle for the string.

### -param format [in]

Type: <b>const <a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a> object that specifies layout information (alignment, trimming, tab stops, and the like) for the string.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

Note that GDI+ does not support PostScript fonts or OpenType fonts which do not have TrueType outlines. 


#### Examples



The following example creates a <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object <i>path</i>, adds a <b>NULL</b>-terminated string to <i>path</i>, and then draws <i>path</i>.


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
      RectF(50.0f, 50.0f, 150.0f, 100.0f),
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



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a>



<a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-text-and-fonts-use">Using Text and Fonts</a>

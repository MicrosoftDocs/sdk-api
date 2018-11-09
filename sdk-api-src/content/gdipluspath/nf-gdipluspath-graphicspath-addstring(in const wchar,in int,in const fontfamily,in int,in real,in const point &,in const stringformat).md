---
UID: NF:gdipluspath.GraphicsPath.AddString(IN const WCHAR,IN INT,IN const FontFamily,IN INT,IN REAL,IN const Point &,IN const StringFormat)
title: GraphicsPath::AddString(IN const WCHAR,IN INT,IN const FontFamily,IN INT,IN REAL,IN const Point &,IN const StringFormat)
author: windows-sdk-content
description: The GraphicsPath::AddString method adds the outlines of a string to this path.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_AddString_WCHAR_string_INT_length_FontFamily_family_INT_style_REAL_emSiz.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\graphicspathaddstringmethods\addstring_58wcharstring_intlength_fontfamilyfamily.htm
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: AddString, AddString method [GDI+], AddString method [GDI+],GraphicsPath class, GraphicsPath class [GDI+],AddString method, GraphicsPath.AddString, GraphicsPath.AddString(IN const WCHAR,IN INT,IN const FontFamily,IN INT,IN REAL,IN const Point &,IN const StringFormat), GraphicsPath.AddString(const WCHAR*,INT,const FontFamily*,INT,REAL,const Point&,const StringFormat*), GraphicsPath::AddString, GraphicsPath::AddString(IN const WCHAR,IN INT,IN const FontFamily,IN INT,IN REAL,IN const Point &,IN const StringFormat), _gdiplus_CLASS_GraphicsPath_AddString_WCHAR_string_INT_length_FontFamily_family_INT_style_REAL_emSiz, gdiplus._gdiplus_CLASS_GraphicsPath_AddString_WCHAR_string_INT_length_FontFamily_family_INT_style_REAL_emSiz
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - GraphicsPath.AddString
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# GraphicsPath::AddString(IN const WCHAR,IN INT,IN const FontFamily,IN INT,IN REAL,IN const Point &,IN const StringFormat)


## -description


The <b>GraphicsPath::AddString</b> method adds the outlines of a string to this path.


## -parameters




### -param string [in]

Type: <b>const WCHAR*</b>

Pointer to a wide-character string. 


### -param length [in]

Type: <b>INT</b>

Integer that specifies the number of characters to display. If the <i>string</i> parameter points to a <b>NULL</b>-terminated string, this parameter can be set to –1. 


### -param family [in]

Type: <b>const <a href="https://msdn.microsoft.com/cdd2ee9e-eb32-420f-8118-50582b55b7cd">FontFamily</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/cdd2ee9e-eb32-420f-8118-50582b55b7cd">FontFamily</a> object that specifies the font family for the string. 


### -param style [in]

Type: <b>INT</b>

Integer that specifies the style of the typeface. This value must be an element of the <a href="https://msdn.microsoft.com/de08c779-1f43-4740-b2b9-8d3906dc4432">FontStyle</a> enumeration or the result of a bitwise 
					<b>OR</b> applied to two or more of these elements. For example, <code>FontStyleBold | FontStyleUnderline | FontStyleStrikeout</code> sets the style as a combination of the three styles. 


### -param emSize [in]

Type: <b>REAL</b>

Real number that specifies the em size, in world units, of the string characters. 


### -param origin [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/8bf4d566-b061-4102-8307-218431e286f8">Point</a></b>

Reference to a <a href="https://msdn.microsoft.com/8bf4d566-b061-4102-8307-218431e286f8">Point</a> object that specifies, in world units, the location of the string. 


### -param format [in]

Type: <b>const <a href="https://msdn.microsoft.com/2d7af5fe-f3e9-4db3-90a5-4e623d9ce773">StringFormat</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/2d7af5fe-f3e9-4db3-90a5-4e623d9ce773">StringFormat</a> object that specifies layout information (alignment, trimming, tab stops, and the like) for the string. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



Note that GDI+ does not support PostScript fonts or OpenType fonts which do not have TrueType outlines. 


#### Examples



The following example creates a <a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a> object <i>path</i>, adds a <b>NULL</b>-terminated string to <i>path</i>, and then draws <i>path</i>.


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
      Point(50, 50),
      NULL);

   Pen pen(Color(255, 255, 0, 0));
   graphics.DrawPath(&pen, &path);
}
```





## -see-also




<a href="https://msdn.microsoft.com/048d67c9-1f57-4b05-b262-7d04ede69267">AddString Methods</a>



<a href="https://msdn.microsoft.com/816a5845-ca03-46c6-bdda-e6a7d02ff614">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/dbfe8cea-bd9e-43ad-85c8-37cce3ef97a4">Constructing and Drawing Paths</a>



<a href="https://msdn.microsoft.com/f6a8085c-3d6a-494f-a1ee-5fa96efb1aae">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/dd8af524-688c-44dd-b3e4-deadb874bdc3">Font</a>



<a href="https://msdn.microsoft.com/cdd2ee9e-eb32-420f-8118-50582b55b7cd">FontFamily</a>



<a href="https://msdn.microsoft.com/de08c779-1f43-4740-b2b9-8d3906dc4432">FontStyle</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a>



<a href="https://msdn.microsoft.com/8bf4d566-b061-4102-8307-218431e286f8">Point</a>



<a href="https://msdn.microsoft.com/2d7af5fe-f3e9-4db3-90a5-4e623d9ce773">StringFormat</a>



<a href="https://msdn.microsoft.com/12bc38c3-5fbc-4d7b-902c-92a5f5057473">Using Text and Fonts</a>
 

 


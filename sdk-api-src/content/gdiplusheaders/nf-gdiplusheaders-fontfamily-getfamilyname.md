---
UID: NF:gdiplusheaders.FontFamily.GetFamilyName
title: FontFamily::GetFamilyName (gdiplusheaders.h)
description: The FontFamily::GetFamilyName method gets the name of this font family.
helpviewer_keywords: ["FontFamily class [GDI+]","GetFamilyName method","FontFamily.GetFamilyName","FontFamily::GetFamilyName","GetFamilyName","GetFamilyName method [GDI+]","GetFamilyName method [GDI+]","FontFamily class","_gdiplus_CLASS_FontFamily_GetFamilyName_name_language_","gdiplus._gdiplus_CLASS_FontFamily_GetFamilyName_name_language_"]
old-location: gdiplus\_gdiplus_CLASS_FontFamily_GetFamilyName_name_language_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\fontfamilyclass\fontfamilymethods\getfamilyname.htm
ms.date: 12/05/2018
ms.keywords: FontFamily class [GDI+],GetFamilyName method, FontFamily.GetFamilyName, FontFamily::GetFamilyName, GetFamilyName, GetFamilyName method [GDI+], GetFamilyName method [GDI+],FontFamily class, _gdiplus_CLASS_FontFamily_GetFamilyName_name_language_, gdiplus._gdiplus_CLASS_FontFamily_GetFamilyName_name_language_
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - FontFamily::GetFamilyName
 - gdiplusheaders/FontFamily::GetFamilyName
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
 - FontFamily.GetFamilyName
---

# FontFamily::GetFamilyName


## -description

The <b>FontFamily::GetFamilyName</b> method gets the name of this font family.

## -parameters

### -param name [out]

Type: <b>WCHAR[LF_FACESIZE]</b>

Name of this font family.

### -param language [in]

Type: <b>WCHAR</b>

Optional. Sixteen-bit value that specifies the language to use. The default value is LANG_NEUTRAL, which is the user's default language.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

When specifying LANG_NEUTRAL as the language ID, it is common practice to pass just LANG_NEUTRAL as in the following example:

<code>stat = FontFamily.GetFamilyName(name, LANG_NEUTRAL);</code>

If you are specifying a language other than LANG_NEUTRAL, use MAKELANGID to create the language and sublanguage combination as in the following example: 

<code>LANGID language = MAKELANGID(LANG_CHINESE, SUBLANG_CHINESE_TRADITIONAL);</code>

For a listing of the available languages and sublanguages, see Winnt.h.


#### Examples

The following example creates a 
						<b>FontFamily</b> object, gets the family name, and outputs the name as text.


```cpp
VOID Example_GetFamilyName(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a FontFamily object.
   FontFamily nameFontFamily(L"arial");
   
   // Get the cell ascent of the font family in design units.
   WCHAR      familyName[LF_FACESIZE];
   nameFontFamily.GetFamilyName(familyName);

   // Copy the cell ascent into a string and draw the string.
   SolidBrush solidbrush(Color(255, 0, 0, 0));
   Font       font(&nameFontFamily, 16);
   graphics.DrawString(familyName, -1, &font, PointF(0, 0), &solidbrush);
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-constructing-font-families-and-fonts-use">Constructing Font Families and Fonts</a>



<a href="/windows/desktop/gdiplus/-gdiplus-enumerating-installed-fonts-use">Enumerating Installed Fonts</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily">FontFamily</a>
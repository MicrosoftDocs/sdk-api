---
UID: NF:gdiplusheaders.FontCollection.GetFamilyCount
title: FontCollection::GetFamilyCount (gdiplusheaders.h)
description: The FontCollection::GetFamilyCount method gets the number of font families contained in this font collection.
helpviewer_keywords: ["FontCollection class [GDI+]","GetFamilyCount method","FontCollection.GetFamilyCount","FontCollection::GetFamilyCount","GetFamilyCount","GetFamilyCount method [GDI+]","GetFamilyCount method [GDI+]","FontCollection class","_gdiplus_CLASS_FontCollection_GetFamilyCount_","gdiplus._gdiplus_CLASS_FontCollection_GetFamilyCount_"]
old-location: gdiplus\_gdiplus_CLASS_FontCollection_GetFamilyCount_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\fontcollectionclass\fontcollectionmethods\getfamilycount.htm
ms.date: 12/05/2018
ms.keywords: FontCollection class [GDI+],GetFamilyCount method, FontCollection.GetFamilyCount, FontCollection::GetFamilyCount, GetFamilyCount, GetFamilyCount method [GDI+], GetFamilyCount method [GDI+],FontCollection class, _gdiplus_CLASS_FontCollection_GetFamilyCount_, gdiplus._gdiplus_CLASS_FontCollection_GetFamilyCount_
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
 - FontCollection::GetFamilyCount
 - gdiplusheaders/FontCollection::GetFamilyCount
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
 - FontCollection.GetFamilyCount
---

# FontCollection::GetFamilyCount


## -description

The <b>FontCollection::GetFamilyCount</b> method gets the number of font families contained in this font collection.



## -returns

Type: <b>INT</b>

This method returns the number of font families contained in this font collection.

## -remarks

A font family consists of a single font type with related styles. An example of a single font type is Arial Regular. An example of a font family is a set of fonts containing Arial Regular, Arial Italic, and Arial Bold style fonts.


#### Examples



The following example creates a <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection">PrivateFontCollection</a> object, gets the number of 
						<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily">FontFamily</a> objects contained within the collection, and outputs that number.


```cpp
VOID Example_GetFamilyCount(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a PrivateFontCollection object, and add three families.
   PrivateFontCollection fontCollection;
   fontCollection.AddFontFile(L"C:\\WINNT\\Fonts\\Arial.ttf");
   fontCollection.AddFontFile(L"C:\\WINNT\\Fonts\\CourBI.ttf");
   fontCollection.AddFontFile(L"C:\\WINNT\\Fonts\\TimesBd.ttf");

   // Get the number of font families in the collection.
   int numFamilies = fontCollection.GetFamilyCount();

   // Print the number of families as text.
   SolidBrush solidbrush(Color(255, 0, 0, 0));
   Font       font(L"Arial", 16);
   WCHAR      string[256];
   swprintf_s(string, L"There are %i families in fontCollection.", numFamilies);
   graphics.DrawString(string,
                       wcslen(string), &font, PointF(0, 0), &solidbrush);
}
```

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontcollection">FontCollection</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection">PrivateFontCollection</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-text-and-fonts-use">Using Text and Fonts</a>

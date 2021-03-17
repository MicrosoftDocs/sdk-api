---
UID: NF:gdiplusheaders.FontCollection.GetFamilies
title: FontCollection::GetFamilies (gdiplusheaders.h)
description: The FontCollection::GetFamilies method gets the font families contained in this font collection.
helpviewer_keywords: ["FontCollection class [GDI+]","GetFamilies method","FontCollection.GetFamilies","FontCollection::GetFamilies","GetFamilies","GetFamilies method [GDI+]","GetFamilies method [GDI+]","FontCollection class","_gdiplus_CLASS_FontCollection_GetFamilies_numSought_gpfamilies_numFound_","gdiplus._gdiplus_CLASS_FontCollection_GetFamilies_numSought_gpfamilies_numFound_"]
old-location: gdiplus\_gdiplus_CLASS_FontCollection_GetFamilies_numSought_gpfamilies_numFound_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\fontcollectionclass\fontcollectionmethods\getfamilies.htm
ms.date: 12/05/2018
ms.keywords: FontCollection class [GDI+],GetFamilies method, FontCollection.GetFamilies, FontCollection::GetFamilies, GetFamilies, GetFamilies method [GDI+], GetFamilies method [GDI+],FontCollection class, _gdiplus_CLASS_FontCollection_GetFamilies_numSought_gpfamilies_numFound_, gdiplus._gdiplus_CLASS_FontCollection_GetFamilies_numSought_gpfamilies_numFound_
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
 - FontCollection::GetFamilies
 - gdiplusheaders/FontCollection::GetFamilies
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
 - FontCollection.GetFamilies
---

# FontCollection::GetFamilies


## -description

The <b>FontCollection::GetFamilies</b> method gets the font families contained in this font collection.

## -parameters

### -param numSought [in]

Type: <b>INT</b>

Integer that specifies the number of font families in this font collection.

### -param gpfamilies [out]

Type: <b><a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily">FontFamily</a>*</b>

Pointer to an array that receives the <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily">FontFamily</a> objects.

### -param numFound [out]

Type: <b>INT*</b>

Pointer to an <b>INT</b> that receives the number of font families found in this collection. This number should be the same as the <i>numSought</i> value.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.  If the method fails, it returns one of the other elements of the <b>Status</b> enumeration.

## -remarks

A font family consists of a single font type with related styles. An example of a single font type is Arial Regular. An example of a font family is a set of fonts containing Arial Regular, Arial Italic, and Arial Bold style fonts.


#### Examples

The following example creates a <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection">PrivateFontCollection</a> object, gets the <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily">FontFamily</a> objects contained within the collection, and uses one of the font families to draw text.


```cpp
VOID Example_GetFamilies(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a PrivateFontCollection object, and add three families.
   PrivateFontCollection fontCollection;
   fontCollection.AddFontFile(L"C:\\WINNT\\Fonts\\Arial.ttf");
   fontCollection.AddFontFile(L"C:\\WINNT\\Fonts\\CourBI.ttf");
   fontCollection.AddFontFile(L"C:\\WINNT\\Fonts\\TimesBd.ttf");

   // Create an array to hold the font families, and get the font families of
   // fontCollection.
   FontFamily families[3];
   int numFamilies;
   fontCollection.GetFamilies(3, families, &numFamilies);

   // Create a Font object from the first FontFamily object in the array.
   Font myFont(&families[0], 16);

   // Use myFont to draw text.
   SolidBrush solidbrush(Color(255, 0, 0, 0));
   WCHAR string[] = L"This is an Arial font";
   graphics.DrawString(string,
                       21, &myFont, PointF(0, 0), &solidbrush);
}
```

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontcollection">FontCollection</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount">FontCollection::GetFamilyCount</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily">FontFamily</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection">PrivateFontCollection</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-text-and-fonts-use">Using Text and Fonts</a>
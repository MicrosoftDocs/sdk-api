---
UID: NF:gdiplusheaders.PrivateFontCollection.AddFontFile
title: PrivateFontCollection::AddFontFile (gdiplusheaders.h)
description: The PrivateFontCollection::AddFontFile method adds a font file to this private font collection.
helpviewer_keywords: ["AddFontFile","AddFontFile method [GDI+]","AddFontFile method [GDI+]","PrivateFontCollection class","PrivateFontCollection class [GDI+]","AddFontFile method","PrivateFontCollection.AddFontFile","PrivateFontCollection::AddFontFile","_gdiplus_CLASS_PrivateFontCollection_AddFontFile_filename_","gdiplus._gdiplus_CLASS_PrivateFontCollection_AddFontFile_filename_"]
old-location: gdiplus\_gdiplus_CLASS_PrivateFontCollection_AddFontFile_filename_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\privatefontcollectionclass\privatefontcollectionmethods\addfontfile.htm
ms.date: 12/05/2018
ms.keywords: AddFontFile, AddFontFile method [GDI+], AddFontFile method [GDI+],PrivateFontCollection class, PrivateFontCollection class [GDI+],AddFontFile method, PrivateFontCollection.AddFontFile, PrivateFontCollection::AddFontFile, _gdiplus_CLASS_PrivateFontCollection_AddFontFile_filename_, gdiplus._gdiplus_CLASS_PrivateFontCollection_AddFontFile_filename_
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
 - PrivateFontCollection::AddFontFile
 - gdiplusheaders/PrivateFontCollection::AddFontFile
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
 - PrivateFontCollection.AddFontFile
---

# PrivateFontCollection::AddFontFile


## -description

The <b>PrivateFontCollection::AddFontFile</b> method adds a font file to this private font collection.

## -parameters

### -param filename [in]

Type: <b>const WCHAR*</b>

Pointer to a wide-character string that specifies the name of a font file.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

When you use the GDI+ API, you must never allow your application to download arbitrary fonts from untrusted sources. 
The operating system requires elevated privileges to assure that all installed fonts are trusted.


#### Examples



The following example creates a <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection">PrivateFontCollection</a> object and adds three font files to the collection. The code then gets the font families that are in the collection and, for each family in the collection, creates a font which is used to draw text.


```cpp
VOID Example_AddFontFile(HDC hdc)
{
   Graphics              graphics(hdc);
   SolidBrush            solidBrush(Color(255, 0, 0, 0));
   INT                   found = 0;
   INT                   count = 0;
   WCHAR                 familyName[50];
   FontFamily*           pFontFamily;
   PrivateFontCollection privateFontCollection;

   // Add three font files to the private collection.
   privateFontCollection.AddFontFile(L"C:\\WINNT\\Fonts\\Arial.ttf");
   privateFontCollection.AddFontFile(L"C:\\WINNT\\Fonts\\Cour.ttf");
   privateFontCollection.AddFontFile(L"C:\\WINNT\\Fonts\\Times.ttf");

   // How many font families are in the private collection?
   count = privateFontCollection.GetFamilyCount();

   // Allocate a buffer to hold the array of FontFamily objects returned by
   // the GetFamilies method.
   pFontFamily = (FontFamily*)malloc(count * sizeof(FontFamily));

   // Get the array of FontFamily objects.
   privateFontCollection.GetFamilies(count, pFontFamily, &found);

   for(INT j = 0; j < found; ++j)
   {
      // Get the font family name.
      pFontFamily[j].GetFamilyName(familyName);
   
      // Pass the family name and the address of the private collection to a
      // Font constructor.
      Font* pFont = new Font(familyName, 16, FontStyleRegular,
                             UnitPixel, &privateFontCollection);

      // Use the font to draw a string.
      graphics.DrawString(
                          L"Hello", 
                          5,          // string length 
                          pFont, 
                          PointF(10.0f, (REAL)j*25), 
                          &solidBrush);

      delete(pFont);
   }

   free(pFontFamily);
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-private-font-collection-use">Creating a Private Font Collection</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-installedfontcollection">InstalledFontCollection</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection">PrivateFontCollection</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-text-and-fonts-use">Using Text and Fonts</a>
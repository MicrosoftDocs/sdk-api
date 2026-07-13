---
UID: NF:gdiplusheaders.FontCollection.GetLastStatus
title: FontCollection::GetLastStatus (gdiplusheaders.h)
description: The FontCollection::GetLastStatus method returns a value that indicates the result of this FontCollection object's previous method call.
helpviewer_keywords: ["FontCollection class [GDI+]","GetLastStatus method","FontCollection.GetLastStatus","FontCollection::GetLastStatus","GetLastStatus","GetLastStatus method [GDI+]","GetLastStatus method [GDI+]","FontCollection class","_gdiplus_CLASS_FontCollection_GetLastStatus_","gdiplus._gdiplus_CLASS_FontCollection_GetLastStatus_"]
old-location: gdiplus\_gdiplus_CLASS_FontCollection_GetLastStatus_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\fontcollectionclass\fontcollectionmethods\getlaststatus_22.htm
ms.date: 12/05/2018
ms.keywords: FontCollection class [GDI+],GetLastStatus method, FontCollection.GetLastStatus, FontCollection::GetLastStatus, GetLastStatus, GetLastStatus method [GDI+], GetLastStatus method [GDI+],FontCollection class, _gdiplus_CLASS_FontCollection_GetLastStatus_, gdiplus._gdiplus_CLASS_FontCollection_GetLastStatus_
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
 - FontCollection::GetLastStatus
 - gdiplusheaders/FontCollection::GetLastStatus
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
 - FontCollection.GetLastStatus
---

# FontCollection::GetLastStatus


## -description

The <b>FontCollection::GetLastStatus</b> method returns a value that indicates the result of this <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontcollection">FontCollection</a> object's previous method call.



## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

The <b>FontCollection::GetLastStatus</b> method returns an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the previous method invoked on this <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontcollection">FontCollection</a> object succeeded, <b>FontCollection::GetLastStatus</b> returns Ok.

If the previous method failed, then <b>FontCollection::GetLastStatus</b> returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration that indicates the nature of the failure.

## -remarks

You can call <b>FontCollection::GetLastStatus</b> immediately after constructing a <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontcollection">FontCollection</a> object to determine whether the constructor succeeded. <b>FontCollection::GetLastStatus</b> returns Ok if the constructor succeeded. Otherwise, it returns a value that indicates the nature of the failure.

Note that the implementation of <b>FontCollection::GetLastStatus</b> in the <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font">Font</a> and <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontcollection">FontCollection</a> classes is different from the implementation of this method in other classes. Also, the implementation of <b>FontCollection::GetLastStatus</b> in the <b>Font</b> class is different from the implementation of <b>FontCollection::GetLastStatus</b> in the <b>FontCollection</b> class.


#### Examples



The following example creates a <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection">PrivateFontCollection</a> object, checks the status of a method call, and, if successful, draws text.


```cpp
VOID Example_GetLastStatus(HDC hdc)
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

   // Verify that the call to GetFamilies was successful.
   Status status = fontCollection.GetLastStatus();

   // If the call was successful, draw text.
   if (status == Ok)
   {
      // Create a Font object from the first FontFamily object in the array.
      Font myFont(&families[0], 16);

      // Use myFont to draw text.
      SolidBrush solidbrush(Color(255, 0, 0, 0));
      WCHAR string[] = L"The call was successful";
      graphics.DrawString(string,
                          23, &myFont, PointF(0, 0), &solidbrush);
   }
}
```

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontcollection">FontCollection</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection">PrivateFontCollection</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-text-and-fonts-use">Using Text and Fonts</a>

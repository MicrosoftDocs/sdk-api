---
UID: NF:gdiplusheaders.FontCollection.GetFamilies
title: FontCollection::GetFamilies
author: windows-sdk-content
description: The FontCollection::GetFamilies method gets the font families contained in this font collection.
old-location: gdiplus\_gdiplus_CLASS_FontCollection_GetFamilies_numSought_gpfamilies_numFound_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\fontcollectionclass\fontcollectionmethods\getfamilies.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FontCollection class [GDI+],GetFamilies method, FontCollection.GetFamilies, FontCollection::GetFamilies, GetFamilies, GetFamilies method [GDI+], GetFamilies method [GDI+],FontCollection class, _gdiplus_CLASS_FontCollection_GetFamilies_numSought_gpfamilies_numFound_, gdiplus._gdiplus_CLASS_FontCollection_GetFamilies_numSought_gpfamilies_numFound_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - FontCollection.GetFamilies
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# FontCollection::GetFamilies


## -description


The <b>FontCollection::GetFamilies</b> method gets the font families contained in this font collection.


## -parameters




### -param numSought [in]

Type: <b>INT</b>

Integer that specifies the number of font families in this font collection.


### -param gpfamilies [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534439(v=VS.85).aspx">FontFamily</a>*</b>

Pointer to an array that receives the <a href="https://msdn.microsoft.com/en-us/library/ms534439(v=VS.85).aspx">FontFamily</a> objects.


### -param numFound [out]

Type: <b>INT*</b>

Pointer to an <b>INT</b> that receives the number of font families found in this collection. This number should be the same as the <i>numSought</i> value.


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.  If the method fails, it returns one of the other elements of the <b>Status</b> enumeration.




## -remarks



A font family consists of a single font type with related styles. An example of a single font type is Arial Regular. An example of a font family is a set of fonts containing Arial Regular, Arial Italic, and Arial Bold style fonts.


#### Examples

The following example creates a <a href="https://msdn.microsoft.com/en-us/library/ms534491(v=VS.85).aspx">PrivateFontCollection</a> object, gets the <a href="https://msdn.microsoft.com/en-us/library/ms534439(v=VS.85).aspx">FontFamily</a> objects contained within the collection, and uses one of the font families to draw text.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_GetFamilies(HDC hdc)
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
   fontCollection.GetFamilies(3, families, &amp;numFamilies);

   // Create a Font object from the first FontFamily object in the array.
   Font myFont(&amp;families[0], 16);

   // Use myFont to draw text.
   SolidBrush solidbrush(Color(255, 0, 0, 0));
   WCHAR string[] = L"This is an Arial font";
   graphics.DrawString(string,
                       21, &amp;myFont, PointF(0, 0), &amp;solidbrush);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534438(v=VS.85).aspx">FontCollection</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536187(v=VS.85).aspx">FontCollection::GetFamilyCount</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534439(v=VS.85).aspx">FontFamily</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534491(v=VS.85).aspx">PrivateFontCollection</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533817(v=VS.85).aspx">Using Text and Fonts</a>
 

 


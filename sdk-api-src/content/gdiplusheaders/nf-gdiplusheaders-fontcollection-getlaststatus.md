---
UID: NF:gdiplusheaders.FontCollection.GetLastStatus
title: FontCollection::GetLastStatus
author: windows-driver-content
description: The FontCollection::GetLastStatus method returns a value that indicates the result of this FontCollection object's previous method call.
old-location: gdiplus\_gdiplus_CLASS_FontCollection_GetLastStatus_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\fontcollectionclass\fontcollectionmethods\getlaststatus_22.htm
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: FontCollection class [GDI+],GetLastStatus method, FontCollection.GetLastStatus, FontCollection::GetLastStatus, GetLastStatus, GetLastStatus method [GDI+], GetLastStatus method [GDI+],FontCollection class, _gdiplus_CLASS_FontCollection_GetLastStatus_, gdiplus._gdiplus_CLASS_FontCollection_GetLastStatus_
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gdiplus.dll
api_name:
-	FontCollection.GetLastStatus
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# FontCollection::GetLastStatus


## -description


The <b>FontCollection::GetLastStatus</b> method returns a value that indicates the result of this <a href="https://msdn.microsoft.com/5e1336ea-cb29-4fa4-85d5-077498a69cb2">FontCollection</a> object's previous method call.


## -parameters






## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

The <b>FontCollection::GetLastStatus</b> method returns an element of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the previous method invoked on this <a href="https://msdn.microsoft.com/5e1336ea-cb29-4fa4-85d5-077498a69cb2">FontCollection</a> object succeeded, <b>FontCollection::GetLastStatus</b> returns Ok.

If the previous method failed, then <b>FontCollection::GetLastStatus</b> returns one of the other elements of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration that indicates the nature of the failure.




## -remarks



You can call <b>FontCollection::GetLastStatus</b> immediately after constructing a <a href="https://msdn.microsoft.com/5e1336ea-cb29-4fa4-85d5-077498a69cb2">FontCollection</a> object to determine whether the constructor succeeded. <b>FontCollection::GetLastStatus</b> returns Ok if the constructor succeeded. Otherwise, it returns a value that indicates the nature of the failure.

Note that the implementation of <b>FontCollection::GetLastStatus</b> in the <a href="https://msdn.microsoft.com/dd8af524-688c-44dd-b3e4-deadb874bdc3">Font</a> and <a href="https://msdn.microsoft.com/5e1336ea-cb29-4fa4-85d5-077498a69cb2">FontCollection</a> classes is different from the implementation of this method in other classes. Also, the implementation of <b>FontCollection::GetLastStatus</b> in the <b>Font</b> class is different from the implementation of <b>FontCollection::GetLastStatus</b> in the <b>FontCollection</b> class.


#### Examples



The following example creates a <a href="https://msdn.microsoft.com/b53cc1cd-9dc8-4e93-9f92-7ebed7d034b6">PrivateFontCollection</a> object, checks the status of a method call, and, if successful, draws text.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_GetLastStatus(HDC hdc)
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

   // Verify that the call to GetFamilies was successful.
   Status status = fontCollection.GetLastStatus();

   // If the call was successful, draw text.
   if (status == Ok)
   {
      // Create a Font object from the first FontFamily object in the array.
      Font myFont(&amp;families[0], 16);

      // Use myFont to draw text.
      SolidBrush solidbrush(Color(255, 0, 0, 0));
      WCHAR string[] = L"The call was successful";
      graphics.DrawString(string,
                          23, &amp;myFont, PointF(0, 0), &amp;solidbrush);
   }
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/5e1336ea-cb29-4fa4-85d5-077498a69cb2">FontCollection</a>



<a href="https://msdn.microsoft.com/b53cc1cd-9dc8-4e93-9f92-7ebed7d034b6">PrivateFontCollection</a>



<a href="https://msdn.microsoft.com/12bc38c3-5fbc-4d7b-902c-92a5f5057473">Using Text and Fonts</a>
 

 


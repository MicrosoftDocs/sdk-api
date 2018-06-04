---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# PrivateFontCollection::AddFontFile


## -description


The <b>PrivateFontCollection::AddFontFile</b> method adds a font file to this private font collection.


## -parameters




### -param filename [in]

Type: <b>const WCHAR*</b>

Pointer to a wide-character string that specifies the name of a font file. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -remarks



When you use the GDI+ API, you must never allow your application to download arbitrary fonts from untrusted sources. 
The operating system requires elevated privileges to assure that all installed fonts are trusted.


#### Examples



The following example creates a <a href="https://msdn.microsoft.com/b53cc1cd-9dc8-4e93-9f92-7ebed7d034b6">PrivateFontCollection</a> object and adds three font files to the collection. The code then gets the font families that are in the collection and, for each family in the collection, creates a font which is used to draw text.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_AddFontFile(HDC hdc)
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
   privateFontCollection.GetFamilies(count, pFontFamily, &amp;found);

   for(INT j = 0; j &lt; found; ++j)
   {
      // Get the font family name.
      pFontFamily[j].GetFamilyName(familyName);
   
      // Pass the family name and the address of the private collection to a
      // Font constructor.
      Font* pFont = new Font(familyName, 16, FontStyleRegular,
                             UnitPixel, &amp;privateFontCollection);

      // Use the font to draw a string.
      graphics.DrawString(
                          L"Hello", 
                          5,          // string length 
                          pFont, 
                          PointF(10.0f, (REAL)j*25), 
                          &amp;solidBrush);

      delete(pFont);
   }

   free(pFontFamily);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ae12afcf-12cc-4c84-9aba-de56fc39437b">Creating a Private Font Collection</a>



<a href="https://msdn.microsoft.com/6c71a3eb-4fbf-45b0-ab35-8756a100af31">InstalledFontCollection</a>



<a href="https://msdn.microsoft.com/b53cc1cd-9dc8-4e93-9f92-7ebed7d034b6">PrivateFontCollection</a>



<a href="https://msdn.microsoft.com/12bc38c3-5fbc-4d7b-902c-92a5f5057473">Using Text and Fonts</a>
 

 


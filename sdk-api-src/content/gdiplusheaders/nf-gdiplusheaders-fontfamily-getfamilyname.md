---
UID: NF:gdiplusheaders.FontFamily.GetFamilyName
title: FontFamily::GetFamilyName
author: windows-sdk-content
description: The FontFamily::GetFamilyName method gets the name of this font family.
old-location: gdiplus\_gdiplus_CLASS_FontFamily_GetFamilyName_name_language_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\fontfamilyclass\fontfamilymethods\getfamilyname.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: FontFamily class [GDI+],GetFamilyName method, FontFamily.GetFamilyName, FontFamily::GetFamilyName, GetFamilyName, GetFamilyName method [GDI+], GetFamilyName method [GDI+],FontFamily class, _gdiplus_CLASS_FontFamily_GetFamilyName_name_language_, gdiplus._gdiplus_CLASS_FontFamily_GetFamilyName_name_language_
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gdiplus.dll
api_name:
-	FontFamily.GetFamilyName
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
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



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -remarks



When specifying LANG_NEUTRAL as the language ID, it is common practice to pass just LANG_NEUTRAL as in the following example:

<code>stat = FontFamily.GetFamilyName(name, LANG_NEUTRAL);</code>

If you are specifying a language other than LANG_NEUTRAL, use MAKELANGID to create the language and sublanguage combination as in the following example: 

<code>LANGID language = MAKELANGID(LANG_CHINESE, SUBLANG_CHINESE_TRADITIONAL);</code>

For a listing of the available languages and sublanguages, see Winnt.h.


#### Examples

The following example creates a 
						<b>FontFamily</b> object, gets the family name, and outputs the name as text.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_GetFamilyName(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a FontFamily object.
   FontFamily nameFontFamily(L"arial");
   
   // Get the cell ascent of the font family in design units.
   WCHAR      familyName[LF_FACESIZE];
   nameFontFamily.GetFamilyName(familyName);

   // Copy the cell ascent into a string and draw the string.
   SolidBrush solidbrush(Color(255, 0, 0, 0));
   Font       font(&amp;nameFontFamily, 16);
   graphics.DrawString(familyName, -1, &amp;font, PointF(0, 0), &amp;solidbrush);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/57428fae-6af4-47a5-a499-717dc378767a">Constructing Font Families and Fonts</a>



<a href="https://msdn.microsoft.com/59598f66-4241-4766-a2f0-5de736de959e">Enumerating Installed Fonts</a>



<a href="https://msdn.microsoft.com/cdd2ee9e-eb32-420f-8118-50582b55b7cd">FontFamily</a>
 

 


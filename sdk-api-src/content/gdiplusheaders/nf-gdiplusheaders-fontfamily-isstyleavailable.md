---
UID: NF:gdiplusheaders.FontFamily.IsStyleAvailable
title: FontFamily::IsStyleAvailable
author: windows-sdk-content
description: The FontFamily::IsStyleAvailable method determines whether the specified style is available for this font family.
old-location: gdiplus\_gdiplus_CLASS_FontFamily_IsStyleAvailable_style_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\fontfamilyclass\fontfamilymethods\isstyleavailable.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: FontFamily class [GDI+],IsStyleAvailable method, FontFamily.IsStyleAvailable, FontFamily::IsStyleAvailable, IsStyleAvailable, IsStyleAvailable method [GDI+], IsStyleAvailable method [GDI+],FontFamily class, _gdiplus_CLASS_FontFamily_IsStyleAvailable_style_, gdiplus._gdiplus_CLASS_FontFamily_IsStyleAvailable_style_
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
 - FontFamily.IsStyleAvailable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- gdiplusheaders.h
: 
- FontFamily.IsStyleAvailable
: 
req.product: GDI+ 1.0
---

# FontFamily::IsStyleAvailable


## -description


The <b>FontFamily::IsStyleAvailable</b> method determines whether the specified style is available for this font family.


## -parameters




### -param style [in]

Type: <b>INT</b>

Integer that specifies the style of the typeface. This value must be an element of the <a href="https://msdn.microsoft.com/de08c779-1f43-4740-b2b9-8d3906dc4432">FontStyle</a> enumeration or the result of a bitwise <b>OR</b> applied to two or more of these elements. For example, <code>FontStyleBold | FontStyleUnderline | FontStyleStrikeout </code> specifies a combination of the three styles. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the style or combination of styles is available, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.




## -remarks



This method returns a misleading result on some third-party fonts. For example, <code>IsStyleAvailable(FontStyleUnderline)</code>  may return <b>FALSE</b> because it is really testing for a regular style font that also is an underlined font: <code>(FontStyleRegular | FontStyleUnderline)</code>. If the font does not have a regular style, the IsStyleAvailable method returns <b>FALSE</b>.


#### Examples



The following example creates a <a href="https://msdn.microsoft.com/cdd2ee9e-eb32-420f-8118-50582b55b7cd">FontFamily</a> object. If the font family has a regular style available, the example draws text.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_IsStyleAvailable(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a FontFamily object.
   FontFamily myFontFamily(L"arial");
   
   // Check to see if the regular style is available.
   BOOL isStyleAvailable = myFontFamily.IsStyleAvailable(FontStyleRegular);

   // If regular style is available, draw text.
   if (isStyleAvailable)
   {
       SolidBrush solidbrush(Color(255, 0, 0, 0));
       Font       font(&amp;myFontFamily, 16);
       WCHAR      string[100];
       swprintf_s(string, L"myFontFamily is available in regular style");
       graphics.DrawString(string,
                           wcslen(string), &amp;font, PointF(0, 0), &amp;solidbrush);
   }
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ae12afcf-12cc-4c84-9aba-de56fc39437b">Creating a Private Font Collection</a>



<a href="https://msdn.microsoft.com/cdd2ee9e-eb32-420f-8118-50582b55b7cd">FontFamily</a>



<a href="https://msdn.microsoft.com/de08c779-1f43-4740-b2b9-8d3906dc4432">FontStyle</a>
 

 


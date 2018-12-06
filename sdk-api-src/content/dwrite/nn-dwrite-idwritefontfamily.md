---
UID: NN:dwrite.IDWriteFontFamily
title: IDWriteFontFamily
author: windows-sdk-content
description: Represents a family of related fonts.
old-location: directwrite\IDWriteFontFamily.htm
tech.root: DirectWrite
ms.assetid: 1fce3d62-af4e-4d2b-a3fd-e534b5fcdb13
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDWriteFontFamily, IDWriteFontFamily interface [Direct Write], IDWriteFontFamily interface [Direct Write],described, directwrite.IDWriteFontFamily, dwrite/IDWriteFontFamily
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteFontFamily
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFontFamily interface


## -description


Represents a family of related fonts.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteFontFamily</b> interface inherits from <a href="https://msdn.microsoft.com/00c41c5f-4405-45ff-98e5-03858dc3056f">IDWriteFontList</a>. <b>IDWriteFontFamily</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteFontFamily</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/89b36a28-c8c7-42aa-89a6-7d8f5ddae3fa">GetFamilyNames</a>
</td>
<td align="left" width="63%">
 Creates a localized strings object that contains the family names for the font family, indexed by locale name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ba5836a5-87ca-43bf-bb18-4498ed2a9619">GetFirstMatchingFont</a>
</td>
<td align="left" width="63%">
 Gets the font that best matches the specified properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/81984e35-7b62-4e14-9ded-45cee49a8921">GetMatchingFonts</a>
</td>
<td align="left" width="63%">
 Gets a list of fonts in the font family ranked in order of how well they match the specified properties.

</td>
</tr>
</table> 


## -remarks



A font family is a set of fonts that share the same family name, such as "Times New Roman", but that differ in features. These feature differences include style, such as italic, and weight, such as bold. 

The following illustration shows examples of fonts that are members of the "Times New Roman" font family.

<img alt="Illustration of italic, bold, and bold italic text from the Times New Roman font family" src="images/FontFamily_for_TimesNewRoman.png"/>
An <b>IDWriteFontFamily</b> object can be retrieved from a font collection using the  <a href="https://msdn.microsoft.com/6104a8ed-378f-4e2b-a0e5-8c0291750e65">IDWriteFontCollection::GetFontFamily</a> method shown in the following example.  <a href="https://msdn.microsoft.com/470c63cc-b50f-4b62-98c0-f7ce183bfcfd">GetFontFamily</a> takes a <b>UINT32</b> index and returns the font family for the font at that index.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>IDWriteFontFamily* pFontFamily = NULL;

// Get the font family.
if (SUCCEEDED(hr))
{
    hr = pFontCollection-&gt;GetFontFamily(i, &amp;pFontFamily);
}
</pre>
</td>
</tr>
</table></span></div>
The font family name is used to specify the font family for text layout and text format objects.  You can get a list of localized font family names from an <b>IDWriteFontFamily</b> object in the form of an <a href="https://msdn.microsoft.com/37bfc613-4128-45aa-b6b2-6163d44378e4">IDWriteLocalizedStrings</a> object by using the <a href="https://msdn.microsoft.com/89b36a28-c8c7-42aa-89a6-7d8f5ddae3fa">IDWriteFontFamily::GetFamilyNames</a> method, as shown in the following code.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>IDWriteLocalizedStrings* pFamilyNames = NULL;

// Get a list of localized strings for the family name.
if (SUCCEEDED(hr))
{
    hr = pFontFamily-&gt;GetFamilyNames(&amp;pFamilyNames);
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/00c41c5f-4405-45ff-98e5-03858dc3056f">IDWriteFontList</a>
 

 


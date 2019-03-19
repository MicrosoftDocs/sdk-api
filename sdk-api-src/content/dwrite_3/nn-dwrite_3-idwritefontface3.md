---
UID: NN:dwrite_3.IDWriteFontFace3
title: IDWriteFontFace3 (dwrite_3.h)
author: windows-sdk-content
description: Represents an absolute reference to a font face.
old-location: directwrite\idwritefontface3.htm
tech.root: DirectWrite
ms.assetid: 1081A005-E4A8-4EE0-AFE0-10BD8D8471DF
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDWriteFontFace3, IDWriteFontFace3 interface [Direct Write], IDWriteFontFace3 interface [Direct Write],described, directwrite.idwritefontface3, dwrite_3/IDWriteFontFace3
ms.topic: interface
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
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
 - IDWriteFontFace3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFontFace3 interface


## -description


Represents an absolute reference to a font face.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteFontFace3</b> interface inherits from <a href="https://msdn.microsoft.com/D74F6472-CEEC-4DF5-83C8-0D65923C8028">IDWriteFontFace2</a>. <b>IDWriteFontFace3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteFontFace3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4cbb6895-3151-c6dd-881e-50d3532c8a14">AreCharactersLocal</a>
</td>
<td align="left" width="63%">
Determines whether the specified characters are local.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e8d5b51d-c5b5-6ea5-eda0-36cc9ec425d3">AreGlyphsLocal</a>
</td>
<td align="left" width="63%">
Determines whether the specified glyphs are local.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/81FBE594-3429-4E61-9A83-513605879D2D">GetFaceNames</a>
</td>
<td align="left" width="63%">
Creates a localized strings object that contains the face names for the font (for example, Regular or Bold), indexed by locale name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/EAA7DF51-5089-4A0B-A0E3-C19FB71EB61E">GetFamilyNames</a>
</td>
<td align="left" width="63%">
Creates a localized strings object that contains the family names for the font family, indexed by locale name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3830951F-B304-4EBC-B8D5-611D1AC87F63">GetFontFaceReference</a>
</td>
<td align="left" width="63%">
Gets a font face reference that identifies this font.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F3CF5E9E-C0EA-4A29-8D42-11873DF5A9F2">GetInformationalStrings</a>
</td>
<td align="left" width="63%">
Gets a localized strings collection that contains the specified informational strings, indexed by locale name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/977AFC97-9747-4FCE-861E-E1C40975B2E9">GetPanose</a>
</td>
<td align="left" width="63%">
Gets the PANOSE values from the font, used for font selection and matching.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9EF4A414-8DD9-431B-81A6-D87F4CF9AA73">GetRecommendedRenderingMode</a>
</td>
<td align="left" width="63%">
Determines the recommended text rendering and grid-fit mode to be used based on the font, size, world transform, and measuring mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A5B2DA7D-8222-440D-A8AF-33B07CE0765C">GetStretch</a>
</td>
<td align="left" width="63%">
Gets the stretch (also known as width) of this font.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/EC47D94B-BF85-4AEE-B3C8-2DCEA7310403">GetStyle</a>
</td>
<td align="left" width="63%">
Gets the style (also known as slope) of this font.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A57873B2-F4B4-4129-96FE-A4CAFBFD537F">GetWeight</a>
</td>
<td align="left" width="63%">
Gets the weight of this font.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BCBC382E-C599-429A-9E00-EAB12D675503">HasCharacter</a>
</td>
<td align="left" width="63%">
Determines whether the font supports the specified character.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7a47f73b-9ce7-f7db-688b-291cebad54bb">IsCharacterLocal</a>
</td>
<td align="left" width="63%">
Determines whether the character is locally downloaded from the font.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/def185b6-a717-5390-8521-46e38335800b">IsGlyphLocal</a>
</td>
<td align="left" width="63%">
Determines whether the glyph is locally downloaded from the font.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/D74F6472-CEEC-4DF5-83C8-0D65923C8028">IDWriteFontFace2</a>
 

 


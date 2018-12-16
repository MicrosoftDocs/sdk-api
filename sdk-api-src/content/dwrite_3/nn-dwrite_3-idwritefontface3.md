---
UID: NN:dwrite_3.IDWriteFontFace3
title: IDWriteFontFace3
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
<a href="https://msdn.microsoft.com/en-us/library/Dn894562(v=VS.85).aspx">AreCharactersLocal</a>
</td>
<td align="left" width="63%">
Determines whether the specified characters are local.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn894563(v=VS.85).aspx">AreGlyphsLocal</a>
</td>
<td align="left" width="63%">
Determines whether the specified glyphs are local.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn894564(v=VS.85).aspx">GetFaceNames</a>
</td>
<td align="left" width="63%">
Creates a localized strings object that contains the face names for the font (for example, Regular or Bold), indexed by locale name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn894565(v=VS.85).aspx">GetFamilyNames</a>
</td>
<td align="left" width="63%">
Creates a localized strings object that contains the family names for the font family, indexed by locale name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn894566(v=VS.85).aspx">GetFontFaceReference</a>
</td>
<td align="left" width="63%">
Gets a font face reference that identifies this font.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn894567(v=VS.85).aspx">GetInformationalStrings</a>
</td>
<td align="left" width="63%">
Gets a localized strings collection that contains the specified informational strings, indexed by locale name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn894568(v=VS.85).aspx">GetPanose</a>
</td>
<td align="left" width="63%">
Gets the PANOSE values from the font, used for font selection and matching.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn894569(v=VS.85).aspx">GetRecommendedRenderingMode</a>
</td>
<td align="left" width="63%">
Determines the recommended text rendering and grid-fit mode to be used based on the font, size, world transform, and measuring mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn894570(v=VS.85).aspx">GetStretch</a>
</td>
<td align="left" width="63%">
Gets the stretch (also known as width) of this font.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn894571(v=VS.85).aspx">GetStyle</a>
</td>
<td align="left" width="63%">
Gets the style (also known as slope) of this font.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn894572(v=VS.85).aspx">GetWeight</a>
</td>
<td align="left" width="63%">
Gets the weight of this font.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn894573(v=VS.85).aspx">HasCharacter</a>
</td>
<td align="left" width="63%">
Determines whether the font supports the specified character.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn894574(v=VS.85).aspx">IsCharacterLocal</a>
</td>
<td align="left" width="63%">
Determines whether the character is locally downloaded from the font.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn894575(v=VS.85).aspx">IsGlyphLocal</a>
</td>
<td align="left" width="63%">
Determines whether the glyph is locally downloaded from the font.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/D74F6472-CEEC-4DF5-83C8-0D65923C8028">IDWriteFontFace2</a>
 

 


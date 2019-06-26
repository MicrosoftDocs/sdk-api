---
UID: NN:dwrite_3.IDWriteFontFace3
title: IDWriteFontFace3 (dwrite_3.h)
author: windows-sdk-content
description: Represents an absolute reference to a font face.
old-location: directwrite\idwritefontface3.htm
tech.root: DirectWrite
ms.assetid: 1081A005-E4A8-4EE0-AFE0-10BD8D8471DF
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDWriteFontFace3, IDWriteFontFace3 interface [Direct Write], IDWriteFontFace3 interface [Direct Write],described, directwrite.idwritefontface3, dwrite_3/IDWriteFontFace3
ms.topic: interface
f1_keywords: 
 - "dwrite_3/IDWriteFontFace3"
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
ms.custom: 19H1
---

# IDWriteFontFace3 interface


## -description


Represents an absolute reference to a font face.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteFontFace3</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/dwrite_2/nn-dwrite_2-idwritefontface2">IDWriteFontFace2</a>. <b>IDWriteFontFace3</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite_3/nf-dwrite_3-idwritefontface3-arecharacterslocal">AreCharactersLocal</a>
</td>
<td align="left" width="63%">
Determines whether the specified characters are local.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite_3/nf-dwrite_3-idwritefontface3-areglyphslocal">AreGlyphsLocal</a>
</td>
<td align="left" width="63%">
Determines whether the specified glyphs are local.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite_3/nf-dwrite_3-idwritefontface3-getfacenames">GetFaceNames</a>
</td>
<td align="left" width="63%">
Creates a localized strings object that contains the face names for the font (for example, Regular or Bold), indexed by locale name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite_3/nf-dwrite_3-idwritefontface3-getfamilynames">GetFamilyNames</a>
</td>
<td align="left" width="63%">
Creates a localized strings object that contains the family names for the font family, indexed by locale name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite_3/nf-dwrite_3-idwritefontface3-getfontfacereference">GetFontFaceReference</a>
</td>
<td align="left" width="63%">
Gets a font face reference that identifies this font.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite_3/nf-dwrite_3-idwritefontface3-getinformationalstrings">GetInformationalStrings</a>
</td>
<td align="left" width="63%">
Gets a localized strings collection that contains the specified informational strings, indexed by locale name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite_3/nf-dwrite_3-idwritefontface3-getpanose">GetPanose</a>
</td>
<td align="left" width="63%">
Gets the PANOSE values from the font, used for font selection and matching.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite_3/nf-dwrite_3-idwritefontface3-getrecommendedrenderingmode">GetRecommendedRenderingMode</a>
</td>
<td align="left" width="63%">
Determines the recommended text rendering and grid-fit mode to be used based on the font, size, world transform, and measuring mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite_3/nf-dwrite_3-idwritefontface3-getstretch">GetStretch</a>
</td>
<td align="left" width="63%">
Gets the stretch (also known as width) of this font.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite_3/nf-dwrite_3-idwritefontface3-getstyle">GetStyle</a>
</td>
<td align="left" width="63%">
Gets the style (also known as slope) of this font.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite_3/nf-dwrite_3-idwritefontface3-getweight">GetWeight</a>
</td>
<td align="left" width="63%">
Gets the weight of this font.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite_3/nf-dwrite_3-idwritefontface3-hascharacter">HasCharacter</a>
</td>
<td align="left" width="63%">
Determines whether the font supports the specified character.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite_3/nf-dwrite_3-idwritefontface3-ischaracterlocal">IsCharacterLocal</a>
</td>
<td align="left" width="63%">
Determines whether the character is locally downloaded from the font.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite_3/nf-dwrite_3-idwritefontface3-isglyphlocal">IsGlyphLocal</a>
</td>
<td align="left" width="63%">
Determines whether the glyph is locally downloaded from the font.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dwrite_2/nn-dwrite_2-idwritefontface2">IDWriteFontFace2</a>
 

 


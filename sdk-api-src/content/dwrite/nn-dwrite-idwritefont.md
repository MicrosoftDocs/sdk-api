---
UID: NN:dwrite.IDWriteFont
title: IDWriteFont (dwrite.h)
description: Represents a physical font in a font collection. This interface is used to create font faces from physical fonts, or to retrieve information such as font face metrics or face names from existing font faces.helpviewer_keywords: ["IDWriteFont","IDWriteFont interface [Direct Write]","IDWriteFont interface [Direct Write]","described","directwrite.IDWriteFont","dwrite/IDWriteFont"]
old-location: directwrite\IDWriteFont.htm
tech.root: DirectWrite
ms.assetid: e29e626f-3e63-4c27-934b-64be51dcf3db
ms.date: 12/05/2018
ms.keywords: IDWriteFont, IDWriteFont interface [Direct Write], IDWriteFont interface [Direct Write],described, directwrite.IDWriteFont, dwrite/IDWriteFont
f1_keywords:
- dwrite/IDWriteFont
dev_langs:
- c++
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
- IDWriteFont
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteFont interface


## -description


 Represents a physical font in a font collection. This interface is used to create font faces from  physical fonts, or  to retrieve information such as  font face metrics or face names from existing font faces.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteFont</b> interface inherits from the <a href="/windows/win32/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDWriteFont</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteFont</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritefont-createfontface">CreateFontFace</a>
</td>
<td align="left" width="63%">
 Creates a font face object for the font.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritefont-getfacenames">GetFaceNames</a>
</td>
<td align="left" width="63%">
 Gets a localized strings collection containing the face names for the font (such as Regular or Bold), indexed by locale name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritefont-getfontfamily">GetFontFamily</a>
</td>
<td align="left" width="63%">
 Gets the font family to which the specified font belongs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritefont-getinformationalstrings">GetInformationalStrings</a>
</td>
<td align="left" width="63%">
 Gets a localized strings collection containing the specified informational strings, indexed by locale name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritefont-getmetrics">GetMetrics</a>
</td>
<td align="left" width="63%">
 Obtains design units and common metrics for the font face.
     These metrics are applicable to all the glyphs within a font face and are used by applications for layout calculations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritefont-getsimulations">GetSimulations</a>
</td>
<td align="left" width="63%">
 Gets a value that indicates what simulations are applied to the specified font.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritefont-getstretch">GetStretch</a>
</td>
<td align="left" width="63%">
 Gets the stretch, or width, of the specified font.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritefont-getstyle">GetStyle</a>
</td>
<td align="left" width="63%">
 Gets the style, or slope, of the specified font.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritefont-getweight">GetWeight</a>
</td>
<td align="left" width="63%">
 Gets the weight, or stroke thickness, of the specified font.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritefont-hascharacter">HasCharacter</a>
</td>
<td align="left" width="63%">
 Determines whether the font supports a specified character.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritefont-issymbolfont">IsSymbolFont</a>
</td>
<td align="left" width="63%">
 Determines whether the font is a symbol font.

</td>
</tr>
</table> 


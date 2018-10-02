---
UID: NN:dwrite.IDWriteFont
title: IDWriteFont
author: windows-sdk-content
description: Represents a physical font in a font collection. This interface is used to create font faces from physical fonts, or to retrieve information such as font face metrics or face names from existing font faces.
old-location: directwrite\IDWriteFont.htm
tech.root: DirectWrite
ms.assetid: e29e626f-3e63-4c27-934b-64be51dcf3db
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IDWriteFont, IDWriteFont interface [Direct Write], IDWriteFont interface [Direct Write],described, directwrite.IDWriteFont, dwrite/IDWriteFont
ms.prod: windows
ms.technology: windows-sdk
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
 - IDWriteFont
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFont interface


## -description


 Represents a physical font in a font collection. This interface is used to create font faces from  physical fonts, or  to retrieve information such as  font face metrics or face names from existing font faces.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteFont</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDWriteFont</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/dd70a9f7-43f3-43e9-94d9-fe70b1b53f59">CreateFontFace</a>
</td>
<td align="left" width="63%">
 Creates a font face object for the font.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6475610a-68f0-4568-9d47-c83515dfa761">GetFaceNames</a>
</td>
<td align="left" width="63%">
 Gets a localized strings collection containing the face names for the font (such as Regular or Bold), indexed by locale name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6104a8ed-378f-4e2b-a0e5-8c0291750e65">GetFontFamily</a>
</td>
<td align="left" width="63%">
 Gets the font family to which the specified font belongs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a23fec10-4027-45eb-9c29-01df385b24e7">GetInformationalStrings</a>
</td>
<td align="left" width="63%">
 Gets a localized strings collection containing the specified informational strings, indexed by locale name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0634d683-2c6e-40cb-94d9-2cf128fc3421">GetMetrics</a>
</td>
<td align="left" width="63%">
 Obtains design units and common metrics for the font face.
     These metrics are applicable to all the glyphs within a font face and are used by applications for layout calculations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3e5ab7f9-0ed2-41d9-b973-a8775ea58358">GetSimulations</a>
</td>
<td align="left" width="63%">
 Gets a value that indicates what simulations are applied to the specified font.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3e90f34a-bbed-4911-9a35-65185db3f162">GetStretch</a>
</td>
<td align="left" width="63%">
 Gets the stretch, or width, of the specified font.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/96d061c7-7d1a-4b3a-bd5f-2bea578de3c4">GetStyle</a>
</td>
<td align="left" width="63%">
 Gets the style, or slope, of the specified font.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/32959881-42f4-45cb-ad32-1acb2787b155">GetWeight</a>
</td>
<td align="left" width="63%">
 Gets the weight, or stroke thickness, of the specified font.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5392119a-dfc3-4947-9a0f-fa66ee6359d6">HasCharacter</a>
</td>
<td align="left" width="63%">
 Determines whether the font supports a specified character.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/08fcbf51-6a88-4d92-848e-dc159d94d1d1">IsSymbolFont</a>
</td>
<td align="left" width="63%">
 Determines whether the font is a symbol font.

</td>
</tr>
</table> 


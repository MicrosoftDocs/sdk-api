---
UID: NN:dwrite.IDWriteTypography
title: IDWriteTypography (dwrite.h)
description: Represents a font typography setting.helpviewer_keywords: ["IDWriteTypography","IDWriteTypography interface [Direct Write]","IDWriteTypography interface [Direct Write]","described","directwrite.IDWriteTypography","dwrite/IDWriteTypography"]
old-location: directwrite\IDWriteTypography.htm
tech.root: DirectWrite
ms.assetid: 061f42db-e9df-4d8c-981f-68d440dfc4c2
ms.date: 12/05/2018
ms.keywords: IDWriteTypography, IDWriteTypography interface [Direct Write], IDWriteTypography interface [Direct Write],described, directwrite.IDWriteTypography, dwrite/IDWriteTypography
f1_keywords:
- dwrite/IDWriteTypography
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
- IDWriteTypography
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteTypography interface


## -description


 Represents a font typography setting.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteTypography</b> interface inherits from the <a href="/windows/win32/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDWriteTypography</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteTypography</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritetypography-addfontfeature">AddFontFeature</a>
</td>
<td align="left" width="63%">
 Adds an OpenType font feature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritetypography-getfontfeature">GetFontFeature</a>
</td>
<td align="left" width="63%">
 Gets the font feature at the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritetypography-getfontfeaturecount">GetFontFeatureCount</a>
</td>
<td align="left" width="63%">
 Gets the number of OpenType font features for the current font.

</td>
</tr>
</table> 


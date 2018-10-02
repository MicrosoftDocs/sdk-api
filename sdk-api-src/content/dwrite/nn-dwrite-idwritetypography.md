---
UID: NN:dwrite.IDWriteTypography
title: IDWriteTypography
author: windows-sdk-content
description: Represents a font typography setting.
old-location: directwrite\IDWriteTypography.htm
tech.root: DirectWrite
ms.assetid: 061f42db-e9df-4d8c-981f-68d440dfc4c2
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IDWriteTypography, IDWriteTypography interface [Direct Write], IDWriteTypography interface [Direct Write],described, directwrite.IDWriteTypography, dwrite/IDWriteTypography
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
 - IDWriteTypography
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTypography interface


## -description


 Represents a font typography setting.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteTypography</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDWriteTypography</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/6d86a66d-a72f-4288-864f-90f877bd166d">AddFontFeature</a>
</td>
<td align="left" width="63%">
 Adds an OpenType font feature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/deb6b466-a654-4bc7-863c-9db32aa4c036">GetFontFeature</a>
</td>
<td align="left" width="63%">
 Gets the font feature at the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/434ea913-00c9-4051-b13c-68f9d67ebd84">GetFontFeatureCount</a>
</td>
<td align="left" width="63%">
 Gets the number of OpenType font features for the current font.

</td>
</tr>
</table> 


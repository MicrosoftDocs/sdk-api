---
UID: NN:dwrite_3.IDWriteFactory3
title: IDWriteFactory3
author: windows-sdk-content
description: The root factory interface for all DirectWrite objects.
old-location: directwrite\idwritefactory3.htm
old-project: DirectWrite
ms.assetid: CCE68F89-6945-40F4-9C27-285AC8AB4D0B
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: IDWriteFactory3, IDWriteFactory3 interface [Direct Write], IDWriteFactory3 interface [Direct Write],described, directwrite.idwritefactory3, dwrite_3/IDWriteFactory3
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: dwrite_3.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteFactory3
product: Windows
targetos: Windows
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDWriteFactory3 interface


## -description


The root factory interface for all <a href="https://msdn.microsoft.com/62a8d723-ae1c-4cbc-a9da-3177e80d4a3a">DirectWrite</a> objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteFactory3</b> interface inherits from <a href="https://msdn.microsoft.com/1D3EEC28-EAB3-4FA2-98E9-7A8FDAF6E6FE">IDWriteFactory2</a>. <b>IDWriteFactory3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteFactory3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/60FA5675-C1E2-40CC-874D-F7E8942165CC">CreateCustomRenderingParams</a>
</td>
<td align="left" width="63%">
Creates a rendering parameters object with the specified properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/22cc005f-6d34-f701-ff83-63ba819ab651">CreateFontCollectionFromFontSet</a>
</td>
<td align="left" width="63%">
Create a weight/width/slope tree from a set of fonts.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e4f73eff-84f8-3e86-08b1-aa513fad9a61">CreateFontFaceReference</a>
</td>
<td align="left" width="63%">Overloaded. Creates a reference to a font.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8021f934-af83-ccd0-e142-455df88bf936">CreateFontSetBuilder</a>
</td>
<td align="left" width="63%">
Creates an empty font set builder to add font face references     
  and create a custom font set. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5BF8BA9C-F07F-43F0-B712-71220E6535A5">CreateGlyphRunAnalysis</a>
</td>
<td align="left" width="63%">
Creates a glyph-run-analysis object that encapsulates info that <a href="https://msdn.microsoft.com/62a8d723-ae1c-4cbc-a9da-3177e80d4a3a">DirectWrite</a> uses to render a glyph run.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/446e4544-b25d-9b59-922c-ca5c896ea99f">GetFontDownloadQueue</a>
</td>
<td align="left" width="63%">
Gets the font download queue associated with this factory object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f6e983b5-5c5f-a2de-59f8-722f967bb992">GetSystemFontCollection</a>
</td>
<td align="left" width="63%">
Retrieves a weight/width/slope tree of system fonts.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/84fd8c9f-f4b1-3015-f431-08b7a07ff32b">GetSystemFontSet</a>
</td>
<td align="left" width="63%">
Retrieves the list of system fonts.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/73a85977-5c24-4abc-ad8c-1d0d6474bd7e">IDWriteFactory</a>



<a href="https://msdn.microsoft.com/1D3EEC28-EAB3-4FA2-98E9-7A8FDAF6E6FE">IDWriteFactory2</a>
 

 


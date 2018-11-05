---
UID: NN:dwrite_2.IDWriteFactory2
title: IDWriteFactory2
author: windows-sdk-content
description: The root factory interface for all DirectWrite objects.
old-location: directwrite\idwritefactory2.htm
tech.root: DirectWrite
ms.assetid: 1D3EEC28-EAB3-4FA2-98E9-7A8FDAF6E6FE
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IDWriteFactory1, IDWriteFactory1 interface [Direct Write], IDWriteFactory1 interface [Direct Write],described, IDWriteFactory2, directwrite.idwritefactory2, dwrite_2/IDWriteFactory2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: dwrite_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
 - IDWriteFactory1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFactory2 interface


## -description


The root factory interface for all <a href="https://msdn.microsoft.com/62a8d723-ae1c-4cbc-a9da-3177e80d4a3a">DirectWrite</a> objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteFactory1</b> interface inherits from <a href="https://msdn.microsoft.com/43FA7E32-FFAD-4F26-A225-811C2CC507DF">IDWriteFactory1</a>. <b>IDWriteFactory2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteFactory1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/947d50fd-888c-2f0b-25c2-b19b0e6fad58">CreateCustomRenderingParams</a>
</td>
<td align="left" width="63%">
Creates a rendering parameters object with the specified properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/98A6DE80-0084-4D28-B456-8E572D565915">CreateFontFallbackBuilder</a>
</td>
<td align="left" width="63%">
Creates a font fallback builder object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/13cecfbf-8bb6-88a2-c8b2-3243f6cb92fd">CreateGlyphRunAnalysis</a>
</td>
<td align="left" width="63%">
Creates a glyph run analysis object, which encapsulates information used to render a glyph run.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7F2BDB39-2CB4-4DB7-BBBA-74B0C07E7420">GetSystemFontFallback</a>
</td>
<td align="left" width="63%">
Creates a font fallback object from the system font fallback list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1D31F807-C3F2-466F-9723-E6F12B13BFA1">TranslateColorGlyphRun</a>
</td>
<td align="left" width="63%">
This method is called on a glyph run to translate it in to multiple color glyph runs.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/73a85977-5c24-4abc-ad8c-1d0d6474bd7e">IDWriteFactory</a>



<a href="https://msdn.microsoft.com/43FA7E32-FFAD-4F26-A225-811C2CC507DF">IDWriteFactory1</a>
 

 


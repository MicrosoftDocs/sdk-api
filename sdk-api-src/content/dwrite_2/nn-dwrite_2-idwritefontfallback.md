---
UID: NN:dwrite_2.IDWriteFontFallback
title: IDWriteFontFallback
author: windows-sdk-content
description: Allows you to access fallback fonts from the font list.
old-location: directwrite\idwritefontfallback.htm
old-project: DirectWrite
ms.assetid: CBC4100A-756B-429E-8368-D5D018A2B0AC
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: IDWriteFontFallback, IDWriteFontFallback interface [Direct Write], IDWriteFontFallback interface [Direct Write],described, directwrite.idwritefontfallback, dwrite_2/IDWriteFontFallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: dwrite_2.h
req.include-header: 
req.redist: 
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
 - IDWriteFontFallback
product: Windows
targetos: Windows
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDWriteFontFallback interface


## -description


Allows you to access fallback fonts from the font list.

The <b>IDWriteFontFallback</b> interface defines a fallback sequence to map character ranges to fonts, which is either created via <a href="https://msdn.microsoft.com/462AC12E-C856-4D8F-83AF-FAC3221425C2">IDWriteFontFallbackBuilder</a> or retrieved from <a href="https://msdn.microsoft.com/7F2BDB39-2CB4-4DB7-BBBA-74B0C07E7420">IDWriteFactory2::GetSystemFontFallback</a>. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteFontFallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDWriteFontFallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteFontFallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9D3DBBF7-72D4-473D-A321-E64BC94493D5">MapCharacters</a>
</td>
<td align="left" width="63%">
Determines an appropriate font to use to render the beginning range of text.

</td>
</tr>
</table> 


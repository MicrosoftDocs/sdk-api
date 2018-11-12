---
UID: NN:dwrite_2.IDWriteFontFallbackBuilder
title: IDWriteFontFallbackBuilder
author: windows-sdk-content
description: Allows you to create Unicode font fallback mappings and create a font fall back object from those mappings.
old-location: directwrite\idwritefontfallbackbuilder.htm
tech.root: DirectWrite
ms.assetid: 462AC12E-C856-4D8F-83AF-FAC3221425C2
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: IDWriteFontFallbackBuilder, IDWriteFontFallbackBuilder interface [Direct Write], IDWriteFontFallbackBuilder interface [Direct Write],described, directwrite.idwritefontfallbackbuilder, dwrite_2/IDWriteFontFallbackBuilder
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
 - IDWriteFontFallbackBuilder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFontFallbackBuilder interface


## -description


Allows you to create Unicode font fallback mappings and create a font fall back object from those mappings.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteFontFallbackBuilder</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDWriteFontFallbackBuilder</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteFontFallbackBuilder</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FCA3CD9C-9FB3-49BD-B4D1-53AEAAAAEE8A">AddMapping</a>
</td>
<td align="left" width="63%">
Appends a single mapping to the list. Call this once for each additional mapping.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8CC8BFD3-4177-4CA0-A74C-43CCDEAA7D74">AddMappings</a>
</td>
<td align="left" width="63%">
Add all the mappings from an existing font fallback object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/933CB690-879E-480E-A0C6-179FA84187F5">CreateFontFallback</a>
</td>
<td align="left" width="63%">
Creates the finalized fallback object from the mappings added.

</td>
</tr>
</table> 


---
UID: NN:dwrite_3.IDWriteFactory5
title: IDWriteFactory5
author: windows-sdk-content
description: The root factory interface for all DirectWrite objects.
old-location: directwrite\idwritefactory5.htm
tech.root: DirectWrite
ms.assetid: 2F3E30DC-A965-4C68-A337-73F338CF2563
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IDWriteFactory5, IDWriteFactory5 interface [Direct Write], IDWriteFactory5 interface [Direct Write],described, directwrite.idwritefactory5, dwrite_3/IDWriteFactory5
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dwrite.lib
 - Dwrite.dll
api_name:
 - IDWriteFactory5
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFactory5 interface


## -description


The root factory interface for all DirectWrite objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteFactory5</b> interface inherits from <a href="https://msdn.microsoft.com/D3C5E48A-A062-430A-A196-CAC621F346FC">IDWriteFactory4</a>. <b>IDWriteFactory5</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteFactory5</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A13656C9-E793-40E2-81BD-0F9C0F437F1E">AnalyzeContainerType</a>
</td>
<td align="left" width="63%">
The AnalyzeContainerType method analyzes the specified file data to determine whether it is a known font container format (e.g., WOFF or WOFF2).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/80E2E906-7596-4E39-808A-5CCA69376903">CreateFontSetBuilder</a>
</td>
<td align="left" width="63%">
Creates an empty font set builder to add font face references and create a custom font set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7C8D581E-489D-48BE-8B3F-278E1C246BBA">CreateHttpFontFileLoader</a>
</td>
<td align="left" width="63%">
Creates a remote font file loader that can create font file references from HTTP or HTTPS URLs. The caller is responsible for registering and unregistering the loader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BA36B91C-C6B8-43B8-BEDA-0089FAE1BAAD">CreateInMemoryFontFileLoader</a>
</td>
<td align="left" width="63%">
Creates a loader object that can be used to create font file references to in-memory fonts. The caller is responsible for registering and unregistering the loader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F82863DC-BFC8-49D3-93C5-DCA45093F81A">UnpackFontFile</a>
</td>
<td align="left" width="63%">
The UnpackFontFile method unpacks font data from a container file (WOFF or WOFF2) and returns the unpacked font data in the form of a font file stream.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/50842838-d150-df9a-f1b7-67ce5ea2bc80">Custom Font Sets</a>



<a href="https://msdn.microsoft.com/D3C5E48A-A062-430A-A196-CAC621F346FC">IDWriteFactory4</a>
 

 


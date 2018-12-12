---
UID: NN:dwrite_3.IDWriteFactory5
title: IDWriteFactory5
author: windows-sdk-content
description: The root factory interface for all DirectWrite objects.
old-location: directwrite\idwritefactory5.htm
tech.root: DirectWrite
ms.assetid: 2F3E30DC-A965-4C68-A337-73F338CF2563
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDWriteFactory5, IDWriteFactory5 interface [Direct Write], IDWriteFactory5 interface [Direct Write],described, directwrite.idwritefactory5, dwrite_3/IDWriteFactory5
ms.prod: windows-hardware
ms.technology: windows-devices
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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteFactory5</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Mt725315(v=VS.85).aspx">IDWriteFactory4</a>. <b>IDWriteFactory5</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Mt807685(v=VS.85).aspx">AnalyzeContainerType</a>
</td>
<td align="left" width="63%">
The AnalyzeContainerType method analyzes the specified file data to determine whether it is a known font container format (e.g., WOFF or WOFF2).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Mt807686(v=VS.85).aspx">CreateFontSetBuilder</a>
</td>
<td align="left" width="63%">
Creates an empty font set builder to add font face references and create a custom font set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Mt807687(v=VS.85).aspx">CreateHttpFontFileLoader</a>
</td>
<td align="left" width="63%">
Creates a remote font file loader that can create font file references from HTTP or HTTPS URLs. The caller is responsible for registering and unregistering the loader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Mt807688(v=VS.85).aspx">CreateInMemoryFontFileLoader</a>
</td>
<td align="left" width="63%">
Creates a loader object that can be used to create font file references to in-memory fonts. The caller is responsible for registering and unregistering the loader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Mt807689(v=VS.85).aspx">UnpackFontFile</a>
</td>
<td align="left" width="63%">
The UnpackFontFile method unpacks font data from a container file (WOFF or WOFF2) and returns the unpacked font data in the form of a font file stream.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/50842838-d150-df9a-f1b7-67ce5ea2bc80">Custom Font Sets</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt725315(v=VS.85).aspx">IDWriteFactory4</a>
 

 


---
UID: NN:dwrite_3.IDWriteFactory3
title: IDWriteFactory3
author: windows-sdk-content
description: The root factory interface for all DirectWrite objects.
old-location: directwrite\idwritefactory3.htm
tech.root: DirectWrite
ms.assetid: CCE68F89-6945-40F4-9C27-285AC8AB4D0B
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDWriteFactory3, IDWriteFactory3 interface [Direct Write], IDWriteFactory3 interface [Direct Write],described, directwrite.idwritefactory3, dwrite_3/IDWriteFactory3
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: dwrite_3.h
req.include-header: 
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
 - IDWriteFactory3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/en-us/library/Dn890754(v=VS.85).aspx">CreateCustomRenderingParams</a>
</td>
<td align="left" width="63%">
Creates a rendering parameters object with the specified properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn890755(v=VS.85).aspx">CreateFontCollectionFromFontSet</a>
</td>
<td align="left" width="63%">
Create a weight/width/slope tree from a set of fonts.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn890758(v=VS.85).aspx">CreateFontFaceReference</a>
</td>
<td align="left" width="63%">Overloaded. Creates a reference to a font.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn890759(v=VS.85).aspx">CreateFontSetBuilder</a>
</td>
<td align="left" width="63%">
Creates an empty font set builder to add font face references     
  and create a custom font set. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn890760(v=VS.85).aspx">CreateGlyphRunAnalysis</a>
</td>
<td align="left" width="63%">
Creates a glyph-run-analysis object that encapsulates info that <a href="https://msdn.microsoft.com/62a8d723-ae1c-4cbc-a9da-3177e80d4a3a">DirectWrite</a> uses to render a glyph run.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn890762(v=VS.85).aspx">GetFontDownloadQueue</a>
</td>
<td align="left" width="63%">
Gets the font download queue associated with this factory object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn890761(v=VS.85).aspx">GetSystemFontCollection</a>
</td>
<td align="left" width="63%">
Retrieves a weight/width/slope tree of system fonts.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn890764(v=VS.85).aspx">GetSystemFontSet</a>
</td>
<td align="left" width="63%">
Retrieves the list of system fonts.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/73a85977-5c24-4abc-ad8c-1d0d6474bd7e">IDWriteFactory</a>



<a href="https://msdn.microsoft.com/1D3EEC28-EAB3-4FA2-98E9-7A8FDAF6E6FE">IDWriteFactory2</a>
 

 


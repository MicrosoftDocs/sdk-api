---
UID: NN:dwrite_3.IDWriteFontSetBuilder
title: IDWriteFontSetBuilder
author: windows-sdk-content
description: Contains methods for building a font set.
old-location: directwrite\idwritefontsetbuilder.htm
tech.root: DirectWrite
ms.assetid: CC6C95CA-BA8B-47C4-A241-650EC8477192
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IDWriteFontSetBuilder, IDWriteFontSetBuilder interface [Direct Write], IDWriteFontSetBuilder interface [Direct Write],described, directwrite.idwritefontsetbuilder, dwrite_3/IDWriteFontSetBuilder
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
 - IDWriteFontSetBuilder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFontSetBuilder interface


## -description


Contains methods for building a font set.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteFontSetBuilder</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDWriteFontSetBuilder</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteFontSetBuilder</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2543720f-1b5a-ca1d-9e24-3fcd61a4de37">AddFontFaceReference</a>
</td>
<td align="left" width="63%">Overloaded. Adds a reference to a font to the set being built.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F8B94A1B-905B-4A96-9943-12BB516311C2">AddFontSet</a>
</td>
<td align="left" width="63%">
Appends an existing font set to the one being built, allowing
        one to aggregate two sets or to essentially extend an existing one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/58923F9C-4DAA-4F97-AE25-A2560176E0F2">CreateFontSet</a>
</td>
<td align="left" width="63%">
Creates a font set from all the font face references added so
        far with AddFontFaceReference.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 


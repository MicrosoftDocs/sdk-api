---
UID: NN:dwrite_3.IDWriteFontSet
title: IDWriteFontSet
author: windows-sdk-content
description: Represents a font set.
old-location: directwrite\idwritefontset.htm
tech.root: DirectWrite
ms.assetid: 0178f248-8dc0-c0ee-63c1-8db3f6ef94c3
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: IDWriteFontSet, IDWriteFontSet interface [Direct Write], IDWriteFontSet interface [Direct Write],described, directwrite.idwritefontset, dwrite_3/IDWriteFontSet
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
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
 - IDWriteFontSet
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFontSet interface


## -description


Represents a font set.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteFontSet</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDWriteFontSet</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteFontSet</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dcb8ddbd-9c82-cd90-f4bd-490855d93efd">FindFontFace</a>
</td>
<td align="left" width="63%">
Gets the index of the matching font face reference in the font set, with the same file, face index, and simulations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dba55a36-8037-5564-59d8-e01189ff0020">FindFontFaceReference</a>
</td>
<td align="left" width="63%">
Gets the index of the matching font face reference in the font set, with the same file, face index, and simulations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/15231d40-9de2-54e4-f4ad-0f1ef9b35c47">GetFontCount</a>
</td>
<td align="left" width="63%">
Get the number of total fonts in the set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8cbc1275-29d5-917d-6938-8fb35e5054fb">GetFontFaceReference</a>
</td>
<td align="left" width="63%">
Gets a reference to the font at the specified index, which may be local or remote.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9f80478e-ed45-58c7-723f-8fe9bd05097b">GetMatchingFonts</a>
</td>
<td align="left" width="63%">Overloaded. Returns a subset of fonts matching the specified criteria.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/514359d4-595d-4cac-a784-527b65b53137">GetPropertyOccurrenceCount</a>
</td>
<td align="left" width="63%">
Returns how many times a given property value occurs in the set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3c3fd5b7-88dd-d434-0b62-f365b407c379">GetPropertyValues</a>
</td>
<td align="left" width="63%">Overloaded. Returns property values for the font set.

</td>
</tr>
</table> 


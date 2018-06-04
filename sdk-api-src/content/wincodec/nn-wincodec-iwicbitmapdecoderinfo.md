---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IWICBitmapDecoderInfo interface


## -description


Exposes methods that provide information about a decoder.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICBitmapDecoderInfo</b> interface inherits from <a href="https://msdn.microsoft.com/502a94bf-3ec4-44d2-b0de-9994f2f9861f">IWICBitmapCodecInfo</a>. <b>IWICBitmapDecoderInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICBitmapDecoderInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2bda1c2a-47b9-4e15-b0c1-52e3f85a6523">CreateInstance</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/91dafd5e-e4fb-4691-a3d0-ca8b6ff0aaf7">IWICBitmapDecoder</a> instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6143a431-cea6-4ced-adf5-2aa4d90d622f">GetPatterns</a>
</td>
<td align="left" width="63%">
Retrieves the file pattern signatures supported by the decoder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/159459a4-f14e-4441-94a6-d55b3bacb868">MatchesPattern</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the codec recognizes the pattern within a specified stream.

</td>
</tr>
</table> 


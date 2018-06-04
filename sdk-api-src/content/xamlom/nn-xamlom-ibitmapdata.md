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

# IBitmapData interface


## -description


Represents an image associated with a node in the visual tree.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBitmapData</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IBitmapData</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBitmapData</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8E8CB014-D394-4457-8AC7-773A87EE2643">CopyBytesTo</a>
</td>
<td align="left" width="63%">
Copies up to the specified maximum number of bytes from the given offset in the bitmap data into the caller’s buffer (<i>pvBytes</i>), and returns the number of bytes copied.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B10BF4E3-C9C2-41E6-99FC-671F6BE47278">GetBitmapDescription</a>
</td>
<td align="left" width="63%">
Gets a <a href="https://msdn.microsoft.com/C5E1BA37-738C-4251-8648-681C58B740E1">BitmapDescription</a> that describes the bitmap data stored in the <b>IBitmapData</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3B11A54C-347D-4F14-A5F8-36250FC5E06B">GetSourceBitmapDescription</a>
</td>
<td align="left" width="63%">
Gets a <a href="https://msdn.microsoft.com/C5E1BA37-738C-4251-8648-681C58B740E1">BitmapDescription</a> that describes the original format of the bitmap data stored in the <b>IBitmapData</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8D4EAB0A-1976-4A40-932C-AAE67F524B94">GetStride</a>
</td>
<td align="left" width="63%">
Gets the stride of the data. This is the length in bytes of each row of the bitmap. 

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 


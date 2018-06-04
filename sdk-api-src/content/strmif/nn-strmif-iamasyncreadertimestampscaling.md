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

# IAMAsyncReaderTimestampScaling interface


## -description


Enables a pull-mode source filter to support larger file sizes.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMAsyncReaderTimestampScaling</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAMAsyncReaderTimestampScaling</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMAsyncReaderTimestampScaling</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2fbadd9d-e741-482f-9ff1-655b149fec49">GetTimestampMode</a>
</td>
<td align="left" width="63%">
Gets the filter's time-stamping mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f556e26-049d-4024-95a2-c899be1ef180">SetTimestampMode</a>
</td>
<td align="left" width="63%">
Sets the filter's time-stamping mode.

</td>
</tr>
</table> 


## -remarks



In the pull model, the parser filter requests data from the source filter by calling <a href="https://msdn.microsoft.com/d0eab370-bb17-48fa-9926-6a6eeaba5603">IAsyncReader::Request</a>. The input to this method is a media sample. The time stamp on the sample specifies the location to read in the stream, as a byte offset.

By default, the time stamp uses the following formula: Time = byte offset × 10000000. This scaling factor limits the effective file size to about 860 GB. To support larger file sizes, call <a href="https://msdn.microsoft.com/7f556e26-049d-4024-95a2-c899be1ef180">SetTimestampMode</a> with the value <b>TRUE</b>. This call sets the scaling factor to 1, so the formula becomes: Time = byte offset.




## -see-also




<a href="https://msdn.microsoft.com/b5246dfe-e6ee-4b91-bfe3-2ec8b8723938">Pull Model</a>
 

 


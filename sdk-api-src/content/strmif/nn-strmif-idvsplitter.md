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

# IDVSplitter interface


## -description



Downgrades the frame rate on a digital video (DV) stream. The <a href="https://msdn.microsoft.com/099d1cc7-f0c5-4c50-a1d5-f2defde7e104">DV Splitter</a> filter exposes this interface.

Applications can use this interface to reduce the frame rate on a DV stream, before the stream reaches the <a href="https://msdn.microsoft.com/aa47010e-8510-475d-836a-cb63deeb3a7b">DV Video Decoder</a> filter. This can be helpful for processor-intensive tasks, such as real-time transcoding.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDVSplitter</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDVSplitter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDVSplitter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/121b94cd-cc39-4ac2-9423-f75df9fcd491">DiscardAlternateVideoFrames</a>
</td>
<td align="left" width="63%">
Discards half of the frames in the video stream.

</td>
</tr>
</table> 


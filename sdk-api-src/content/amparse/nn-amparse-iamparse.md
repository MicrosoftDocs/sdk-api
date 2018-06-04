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

# IAMParse interface


## -description



The <code>IAMParse</code> interface sets and retrieves the <i>parse time</i> for an MPEG-2 stream. The parse time is a notional time associated with the current position in the stream of bytes supplied to the parser filter. This time is also tied to the origin of the time stamps in that time stamp zero corresponds to parse time zero.

The <a href="https://msdn.microsoft.com/06704a5a-e7ae-4187-ae36-32512d951aaf">MPEG-2 Splitter</a> filter implements this interface. Use this interface to retrieve or set the current stream parse time or to clear the data buffer of its current data.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMParse</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAMParse</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMParse</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh463886">Flush</a>
</td>
<td align="left" width="63%">
Empties the current file buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ce87e39e-1e5d-4098-8431-ea9b3188784e">GetParseTime</a>
</td>
<td align="left" width="63%">
Retrieves the current stream parse time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/52c53994-7cb7-4f50-a00d-87faa309c717">SetParseTime</a>
</td>
<td align="left" width="63%">
Sets the current stream parse time.

</td>
</tr>
</table> 


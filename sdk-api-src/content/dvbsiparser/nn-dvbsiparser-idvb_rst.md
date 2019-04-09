---
UID: NN:dvbsiparser.IDVB_RST
title: IDVB_RST (dvbsiparser.h)
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvb_rst.htm
tech.root: mstv
ms.assetid: deee44cb-92b8-4d10-91d7-c99324ab5832
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDVB_RST, IDVB_RST interface [Microsoft TV Technologies], IDVB_RST interface [Microsoft TV Technologies],described, IDVB_RSTInterface, dvbsiparser/IDVB_RST, mstv.idvb_rst
ms.topic: interface
req.header: dvbsiparser.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IDVB_RST
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDVB_RST interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IDVB_RST</b> interface enables the client to get information from a running status table (RST). The <a href="https://msdn.microsoft.com/263abb39-3f8d-4501-985c-d5ac9b1c9ea1">IDvbSiParser::GetRST</a> method returns a pointer to this interface. The RST enables the provider to update the timing status for one or more events, which may be needed if the schedule changes.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDVB_RST</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDVB_RST</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDVB_RST</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/98e71d2e-d84e-4be5-b779-0d7c10a823d5">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Returns the number of records in the RST.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4263160a-dd00-42a8-9ed3-6b266c0d6355">GetRecordEventId</a>
</td>
<td align="left" width="63%">
Returns the event identifier for a record in the RST.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/949dafeb-f59d-4507-a3eb-4a381f4108ff">GetRecordOriginalNetworkId</a>
</td>
<td align="left" width="63%">
Returns the original network identifier for a record in the RST.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ca0a0b3b-14a8-4456-85a0-51df559d04b8">GetRecordRunningStatus</a>
</td>
<td align="left" width="63%">
Returns the running status for a record in the RST.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f9592e18-5cf6-4359-9654-2535070cdce9">GetRecordServiceId</a>
</td>
<td align="left" width="63%">
Returns the service identifier for a record in the RST.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40fd889e-eae8-4532-935e-07a7a5b2b6c2">GetRecordTransportStreamId</a>
</td>
<td align="left" width="63%">
Returns the transport stream identifier (TSID) for a record in the RST.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8efbb9c0-8b21-476c-88ad-1c8a5408b32f">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 


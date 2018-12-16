---
UID: NN:dvbsiparser.IIsdbSiParser2
title: IIsdbSiParser2
author: windows-sdk-content
description: Implements methods that retrieve program specific information (PSI) tables and service information tables from an Integrated Services Digital Broadcast (ISDB) transport stream.
old-location: mstv\iisdbsiparser2.htm
tech.root: mstv
ms.assetid: d8dfc713-aaa4-46b1-8eca-2e132a9d705f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IIsdbSiParser2, IIsdbSiParser2 interface [Microsoft TV Technologies], IIsdbSiParser2 interface [Microsoft TV Technologies],described, dvbsiparser/IIsdbSiParser2, mstv.iisdbsiparser2
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
req.idl: Dvbsiparser.idl
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
 - IIsdbSiParser2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IIsdbSiParser2 interface


## -description


Implements methods that retrieve program specific information (PSI) tables and service information tables from an Integrated Services Digital Broadcast (ISDB) transport stream.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IIsdbSiParser2</b> interface inherits from <b>IDvbSiParser2</b>. <b>IIsdbSiParser2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IIsdbSiParser2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/25993059-a1a9-486f-97b3-fd240c8931dc">GetBIT</a>
</td>
<td align="left" width="63%">
 Retrieves the broadcaster information table (BIT) from an ISDB transport stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c984a340-d31b-43a5-baac-323629002aab">GetCDT</a>
</td>
<td align="left" width="63%">
Retrieves the common data table (CDT) from an ISDB transport stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9dc2aaa9-50f0-4c72-a252-3757a1aa13b7">GetEMM</a>
</td>
<td align="left" width="63%">
Retrieves the entitlement management message (EMM) table  from an ISDB transport stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b4b91e95-cf0f-488b-9941-4d1d81dc7661">GetLDT</a>
</td>
<td align="left" width="63%">
Retrieves the linked description table (LDT)
  from an ISDB transport stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/90c47d88-b364-4b42-b51b-dfa3c9eed4b0">GetNBIT</a>
</td>
<td align="left" width="63%">
 Retrieves the
   network broadcaster information table (NBIT) from an ISDB transport stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d15d1b6a-5b53-4962-89a3-9bd06e00d366">GetSDT</a>
</td>
<td align="left" width="63%">
Retrieves the service description table (SDT) from an ISDB transport stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fd361526-eb0c-4edd-b346-3bded48fdc06">GetSDTT</a>
</td>
<td align="left" width="63%">
Retrieves the  software download
  trigger table
  (SDTT)  from an ISDB transport stream.

</td>
</tr>
</table> 


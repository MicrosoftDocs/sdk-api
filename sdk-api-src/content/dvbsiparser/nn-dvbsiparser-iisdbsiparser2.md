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


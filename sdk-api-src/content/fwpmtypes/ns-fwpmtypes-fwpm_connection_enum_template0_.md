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

# FWPM_CONNECTION_ENUM_TEMPLATE0_ structure


## -description


The <b>FWPM_CONNECTION_ENUM_TEMPLATE0</b> structure is used for limiting connection object enumerations.


## -struct-fields




### -field connectionId

Uniquely identifies a connection object.


### -field flags

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FWPM_CONNECTION_ENUM_FLAG_QUERY_BYTES_TRANSFERRED"></a><a id="fwpm_connection_enum_flag_query_bytes_transferred"></a><dl>
<dt><b>FWPM_CONNECTION_ENUM_FLAG_QUERY_BYTES_TRANSFERRED</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
If set, the IPsec driver will be queried for the current bytes transferred via this connection (allowing monitoring tools to collect accurate data without requiring that querying capabilities remain constantly on). 

</td>
</tr>
</table>
 


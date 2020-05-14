---
UID: NS:fwpmtypes.FWPM_CONNECTION_ENUM_TEMPLATE0_
title: FWPM_CONNECTION_ENUM_TEMPLATE0 (fwpmtypes.h)
description: Used for limiting connection object enumerations.helpviewer_keywords: ["FWPM_CONNECTION_ENUM_FLAG_QUERY_BYTES_TRANSFERRED","FWPM_CONNECTION_ENUM_TEMPLATE0","FWPM_CONNECTION_ENUM_TEMPLATE0 structure [Filtering]","fwp.fwpm_connection_enum_template0","fwpmtypes/FWPM_CONNECTION_ENUM_TEMPLATE0"]
old-location: fwp\fwpm_connection_enum_template0.htm
tech.root: fwp
ms.assetid: 1939e4ae-9ff8-4ee7-895b-2ed992204b5c
ms.date: 12/05/2018
ms.keywords: FWPM_CONNECTION_ENUM_FLAG_QUERY_BYTES_TRANSFERRED, FWPM_CONNECTION_ENUM_TEMPLATE0, FWPM_CONNECTION_ENUM_TEMPLATE0 structure [Filtering], fwp.fwpm_connection_enum_template0, fwpmtypes/FWPM_CONNECTION_ENUM_TEMPLATE0
f1_keywords:
- fwpmtypes/FWPM_CONNECTION_ENUM_TEMPLATE0
dev_langs:
- c++
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fwpmtypes.idl
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
- HeaderDef
api_location:
- Fwpmtypes.h
api_name:
- FWPM_CONNECTION_ENUM_TEMPLATE0
targetos: Windows
req.typenames: FWPM_CONNECTION_ENUM_TEMPLATE0
req.redist: 
ms.custom: 19H1
---

# FWPM_CONNECTION_ENUM_TEMPLATE0 structure


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
 


---
UID: NS:netioapi._MIB_IPFORWARD_TABLE2
title: MIB_IPFORWARD_TABLE2 (netioapi.h)
description: Contains a table of IP route entries.
helpviewer_keywords: ["*PMIB_IPFORWARD_TABLE2","MIB_IPFORWARD_TABLE2","MIB_IPFORWARD_TABLE2 structure [MIB]","PMIB_IPFORWARD_TABLE2","PMIB_IPFORWARD_TABLE2 structure pointer [MIB]","mib.mib_ipforward_table2","netioapi/MIB_IPFORWARD_TABLE2","netioapi/PMIB_IPFORWARD_TABLE2"]
old-location: mib\mib_ipforward_table2.htm
tech.root: MIB
ms.assetid: 9ba938e8-3395-4c9d-b1d2-b2c030783c16
ms.date: 12/05/2018
ms.keywords: '*PMIB_IPFORWARD_TABLE2, MIB_IPFORWARD_TABLE2, MIB_IPFORWARD_TABLE2 structure [MIB], PMIB_IPFORWARD_TABLE2, PMIB_IPFORWARD_TABLE2 structure pointer [MIB], mib.mib_ipforward_table2, netioapi/MIB_IPFORWARD_TABLE2, netioapi/PMIB_IPFORWARD_TABLE2'
req.header: netioapi.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
targetos: Windows
req.typenames: MIB_IPFORWARD_TABLE2, *PMIB_IPFORWARD_TABLE2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_IPFORWARD_TABLE2
 - netioapi/_MIB_IPFORWARD_TABLE2
 - PMIB_IPFORWARD_TABLE2
 - netioapi/PMIB_IPFORWARD_TABLE2
 - MIB_IPFORWARD_TABLE2
 - netioapi/MIB_IPFORWARD_TABLE2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Netioapi.h
api_name:
 - MIB_IPFORWARD_TABLE2
---

# MIB_IPFORWARD_TABLE2 structure


## -description

The 
<b>MIB_IPFORWARD_TABLE2</b> structure contains a table of IP route entries.

## -struct-fields

### -field NumEntries

A value that specifies the number of IP route entries in the array.

### -field Table

An array of 
<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipforward_row2">MIB_IPFORWARD_ROW2</a> structures containing IP route entries.

## -remarks

The <b>MIB_IPFORWARD_TABLE2</b> structure is defined on Windows Vista and later. 

The <b>GetIpForwardTable2</b> function enumerates the IP route entries on a local system and returns this information in a <b>MIB_IPFORWARD_TABLE2</b> structure. 



The <b>GetIpForwardEntry2</b> function retrieves a single IP route entry and returns this information in a <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipforward_row2">MIB_IPFORWARD_ROW2</a> structure.

The <b>MIB_IPFORWARD_TABLE2</b> structure may contain padding for alignment between the <b>NumEntries</b> member and the first <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipforward_row2">MIB_IPFORWARD_ROW2</a> array entry in the <b>Table</b> member. Padding for alignment may also be present between the <b>MIB_IPFORWARD_ROW2</b> array entries in the <b>Table</b> member. Any access to a <b>MIB_IPFORWARD_ROW2</b> array entry should assume  padding may exist. 



Note that the <i>Netioapi.h</i> header file is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Netioapi.h</i> header file should never be used directly.

## -see-also

<b>GetIpForwardEntry2</b>



<b>GetIpForwardTable2</b>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipforward_row2">MIB_IPFORWARD_ROW2</a>
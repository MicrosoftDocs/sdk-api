---
UID: NS:netioapi._MIB_IF_TABLE2
title: MIB_IF_TABLE2 (netioapi.h)
description: Contains a table of logical and physical interface entries.
helpviewer_keywords: ["*PMIB_IF_TABLE2","MIB_IF_TABLE2","MIB_IF_TABLE2 structure [MIB]","PMIB_IF_TABLE2","PMIB_IF_TABLE2 structure pointer [MIB]","_MIB_IF_TABLE2","mib.mib_if_table2","netioapi/MIB_IF_TABLE2","netioapi/PMIB_IF_TABLE2"]
old-location: mib\mib_if_table2.htm
tech.root: MIB
ms.assetid: 334078c6-afd0-4c53-838c-28bc3e1e8484
ms.date: 12/05/2018
ms.keywords: '*PMIB_IF_TABLE2, MIB_IF_TABLE2, MIB_IF_TABLE2 structure [MIB], PMIB_IF_TABLE2, PMIB_IF_TABLE2 structure pointer [MIB], _MIB_IF_TABLE2, mib.mib_if_table2, netioapi/MIB_IF_TABLE2, netioapi/PMIB_IF_TABLE2'
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
req.typenames: MIB_IF_TABLE2, *PMIB_IF_TABLE2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_IF_TABLE2
 - netioapi/_MIB_IF_TABLE2
 - PMIB_IF_TABLE2
 - netioapi/PMIB_IF_TABLE2
 - MIB_IF_TABLE2
 - netioapi/MIB_IF_TABLE2
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
 - MIB_IF_TABLE2
---

# MIB_IF_TABLE2 structure


## -description

The 
<b>MIB_IF_TABLE2</b> structure contains a table of logical and physical interface entries.

## -struct-fields

### -field NumEntries

The number of interface entries in the array.

### -field Table

An array of 
<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2">MIB_IF_ROW2</a> structures containing interface entries.

## -remarks

The <b>MIB_IF_TABLE2</b> structure is defined in Windows Vista and later. 

The <a href="/windows/desktop/api/netioapi/nf-netioapi-getiftable2">GetIfTable2</a> and <a href="/windows/desktop/api/netioapi/nf-netioapi-getiftable2ex">GetIfTable2Ex</a> functions enumerates the logical and physical interfaces on a local system and returns this information in a <b>MIB_IF_TABLE2</b> structure. 



The <b>MIB_IF_TABLE2</b> structure may contain padding for alignment between the <b>NumEntries</b> member and the first <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2">MIB_IF_ROW2</a> array entry in the <b>Table</b> member. Padding for alignment may also be present between the <b>MIB_IF_ROW2</b> array entries in the <b>Table</b> member. Any access to a <b>MIB_IF_ROW2</b> array entry should assume  padding may exist. 



Note that the <i>Netioapi.h</i> header file is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Netioapi.h</i> header file should never be used directly.

## -see-also

<a href="/windows/desktop/api/netioapi/nf-netioapi-getiftable2">GetIfTable2</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getiftable2ex">GetIfTable2Ex</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2">MIB_IF_ROW2</a>
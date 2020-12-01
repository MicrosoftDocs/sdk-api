---
UID: NS:netioapi._MIB_IPPATH_TABLE
title: MIB_IPPATH_TABLE (netioapi.h)
description: Contains a table of IP path entries.
helpviewer_keywords: ["*PMIB_IPPATH_TABLE","MIB_IPPATH_TABLE","MIB_IPPATH_TABLE structure [MIB]","PMIB_IPPATH_TABLE","PMIB_IPPATH_TABLE structure pointer [MIB]","_MIB_IPPATH_TABLE","mib.mib_ippath_table","netioapi/MIB_IPPATH_TABLE","netioapi/PMIB_IPPATH_TABLE"]
old-location: mib\mib_ippath_table.htm
tech.root: MIB
ms.assetid: f18aff3c-a7b5-40fa-9308-5bd8821c77e2
ms.date: 12/05/2018
ms.keywords: '*PMIB_IPPATH_TABLE, MIB_IPPATH_TABLE, MIB_IPPATH_TABLE structure [MIB], PMIB_IPPATH_TABLE, PMIB_IPPATH_TABLE structure pointer [MIB], _MIB_IPPATH_TABLE, mib.mib_ippath_table, netioapi/MIB_IPPATH_TABLE, netioapi/PMIB_IPPATH_TABLE'
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
req.typenames: MIB_IPPATH_TABLE, *PMIB_IPPATH_TABLE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_IPPATH_TABLE
 - netioapi/_MIB_IPPATH_TABLE
 - PMIB_IPPATH_TABLE
 - netioapi/PMIB_IPPATH_TABLE
 - MIB_IPPATH_TABLE
 - netioapi/MIB_IPPATH_TABLE
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
 - MIB_IPPATH_TABLE
---

# MIB_IPPATH_TABLE structure


## -description

The 
<b>MIB_IPPATH_TABLE</b> structure contains a table of IP path entries.

## -struct-fields

### -field NumEntries

A value that specifies the number of IP path entries in the array.

### -field Table

An array of 
<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ippath_row">MIB_IPPATH_ROW</a> structures containing IP path entries.

## -remarks

The <b>MIB_IPPATH_TABLE</b> structure is defined on Windows Vista and later. 

The <a href="/windows/desktop/api/netioapi/nf-netioapi-getippathtable">GetIpPathTable</a> function enumerates the IP path entries on a local system and returns this information in a <b>MIB_IPPATH_TABLE</b> structure. 

The <a href="/windows/desktop/api/netioapi/nf-netioapi-flushippathtable">FlushIpPathTable</a> function flushes the IP path table entries on a local system. 



The <a href="/windows/desktop/api/netioapi/nf-netioapi-getippathentry">GetIpPathEntry</a> function retrieves a single IP path entry and returns this information in a <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ippath_row">MIB_IPPATH_ROW</a> structure.

The <b>MIB_IPPATH_TABLE</b> structure may contain padding for alignment between the <b>NumEntries</b> member and the first <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ippath_row">MIB_IPPATH_ROW</a> array entry in the <b>Table</b> member. Padding for alignment may also be present between the <b>MIB_IPPATH_ROW</b> array entries in the <b>Table</b> member. Any access to a <b>MIB_IPPATH_ROW</b> array entry should assume  padding may exist.

## -see-also

<a href="/windows/desktop/api/netioapi/nf-netioapi-flushippathtable">FlushIpPathTable</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getippathentry">GetIpPathEntry</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getippathtable">GetIpPathTable</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ippath_row">MIB_IPPATH_ROW</a>
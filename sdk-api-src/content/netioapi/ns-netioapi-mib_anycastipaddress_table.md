---
UID: NS:netioapi._MIB_ANYCASTIPADDRESS_TABLE
title: MIB_ANYCASTIPADDRESS_TABLE (netioapi.h)
description: Contains a table of anycast IP address entries.
helpviewer_keywords: ["*PMIB_ANYCASTIPADDRESS_TABLE","MIB_ANYCASTIPADDRESS_TABLE","MIB_ANYCASTIPADDRESS_TABLE structure [MIB]","PMIB_ANYCASTIPADDRESS_TABLE","PMIB_ANYCASTIPADDRESS_TABLE structure pointer [MIB]","_MIB_ANYCASTIPADDRESS_TABLE","mib.mib_anycastipaddress_table","netioapi/MIB_ANYCASTIPADDRESS_TABLE","netioapi/PMIB_ANYCASTIPADDRESS_TABLE"]
old-location: mib\mib_anycastipaddress_table.htm
tech.root: MIB
ms.assetid: 46b99759-eb9a-4f91-a6b6-40e6e9f55038
ms.date: 12/05/2018
ms.keywords: '*PMIB_ANYCASTIPADDRESS_TABLE, MIB_ANYCASTIPADDRESS_TABLE, MIB_ANYCASTIPADDRESS_TABLE structure [MIB], PMIB_ANYCASTIPADDRESS_TABLE, PMIB_ANYCASTIPADDRESS_TABLE structure pointer [MIB], _MIB_ANYCASTIPADDRESS_TABLE, mib.mib_anycastipaddress_table, netioapi/MIB_ANYCASTIPADDRESS_TABLE, netioapi/PMIB_ANYCASTIPADDRESS_TABLE'
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
req.typenames: MIB_ANYCASTIPADDRESS_TABLE, *PMIB_ANYCASTIPADDRESS_TABLE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_ANYCASTIPADDRESS_TABLE
 - netioapi/_MIB_ANYCASTIPADDRESS_TABLE
 - PMIB_ANYCASTIPADDRESS_TABLE
 - netioapi/PMIB_ANYCASTIPADDRESS_TABLE
 - MIB_ANYCASTIPADDRESS_TABLE
 - netioapi/MIB_ANYCASTIPADDRESS_TABLE
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
 - MIB_ANYCASTIPADDRESS_TABLE
---

# MIB_ANYCASTIPADDRESS_TABLE structure


## -description

The 
<b>MIB_ANYCASTIPADDRESS_TABLE</b> structure contains a table of anycast IP address entries.

## -struct-fields

### -field NumEntries

A value that specifies the number of anycast IP address entries in the array.

### -field Table

An array of 
<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_anycastipaddress_row">MIB_ANYCASTIPADDRESS_ROW</a> structures containing anycast IP address entries.

## -remarks

The <b>MIB_ANYCASTIPADDRESS_TABLE</b> structure is defined on Windows Vista and later. 

The <a href="/windows/desktop/api/netioapi/nf-netioapi-getanycastipaddresstable">GetAnycastIpAddressTable</a> function enumerates the anycast IP addresses on a local system and returns this information in a <b>MIB_ANYCASTIPADDRESS_TABLE</b> structure. 



The <b>MIB_ANYCASTIPADDRESS_TABLE</b> structure may contain padding for alignment between the <b>NumEntries</b> member and the first <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_anycastipaddress_row">MIB_ANYCASTIPADDRESS_ROW</a> array entry in the <b>Table</b> member. Padding for alignment may also be present between the <b>MIB_ANYCASTIPADDRESS_ROW</b> array entries in the <b>Table</b> member. Any access to a <b>MIB_ANYCASTIPADDRESS_ROW</b> array entry should assume  padding may exist. 



Note that the <i>Netioapi.h</i> header file is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Netioapi.h</i> header file should never be used directly.

## -see-also

<a href="/windows/desktop/api/netioapi/nf-netioapi-getanycastipaddresstable">GetAnycastIpAddressTable</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_anycastipaddress_row">MIB_ANYCASTIPADDRESS_ROW</a>
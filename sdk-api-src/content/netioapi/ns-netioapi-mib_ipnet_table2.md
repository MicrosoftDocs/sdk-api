---
UID: NS:netioapi._MIB_IPNET_TABLE2
title: MIB_IPNET_TABLE2 (netioapi.h)
description: Contains a table of neighbor IP address entries.
helpviewer_keywords: ["*PMIB_IPNET_TABLE2","MIB_IPNET_TABLE2","MIB_IPNET_TABLE2 structure [MIB]","PMIB_IPNET_TABLE2","PMIB_IPNET_TABLE2 structure pointer [MIB]","_MIB_IPNET_TABLE2","mib.mib_ipnet_table2","netioapi/MIB_IPNET_TABLE2","netioapi/PMIB_IPNET_TABLE2"]
old-location: mib\mib_ipnet_table2.htm
tech.root: MIB
ms.assetid: 39b87d81-69ce-4f9b-8af6-5e0c5051657c
ms.date: 12/05/2018
ms.keywords: '*PMIB_IPNET_TABLE2, MIB_IPNET_TABLE2, MIB_IPNET_TABLE2 structure [MIB], PMIB_IPNET_TABLE2, PMIB_IPNET_TABLE2 structure pointer [MIB], _MIB_IPNET_TABLE2, mib.mib_ipnet_table2, netioapi/MIB_IPNET_TABLE2, netioapi/PMIB_IPNET_TABLE2'
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
req.typenames: MIB_IPNET_TABLE2, *PMIB_IPNET_TABLE2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_IPNET_TABLE2
 - netioapi/_MIB_IPNET_TABLE2
 - PMIB_IPNET_TABLE2
 - netioapi/PMIB_IPNET_TABLE2
 - MIB_IPNET_TABLE2
 - netioapi/MIB_IPNET_TABLE2
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
 - MIB_IPNET_TABLE2
---

# MIB_IPNET_TABLE2 structure


## -description

The 
<b>MIB_IPNET_TABLE2</b> structure contains a table of neighbor IP address entries.

## -struct-fields

### -field NumEntries

A value that specifies the number of IP network neighbor address entries in the array.

### -field Table

An array of 
<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipnet_row2">MIB_IPNET_ROW2</a> structures containing IP network neighbor address entries.

## -remarks

The <b>MIB_IPNET_TABLE2</b> structure is defined on Windows Vista and later. 

The <a href="/windows/desktop/api/netioapi/nf-netioapi-getipnettable2">GetIpNetTable2</a> function enumerates the neighbor IP addresses on a local system and returns this information in an <b>MIB_IPNET_TABLE2</b> structure. 

For IPv4, this includes addresses determined used the Address Resolution Protocol (ARP). For IPv6, this includes addresses determined using the Neighbor Discovery (ND) protocol for IPv6 as specified in RFC 2461. For more information, see <a href="https://www.ietf.org/rfc/rfc2461.txt">http://www.ietf.org/rfc/rfc2461.txt</a>. 

The <b>MIB_IPNET_TABLE2</b> structure may contain padding for alignment between the <b>NumEntries</b> member and the first <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipnet_row2">MIB_IPNET_ROW2</a> array entry in the <b>Table</b> member. Padding for alignment may also be present between the <b>MIB_IPNET_ROW2</b> array entries in the <b>Table</b> member. Any access to a <b>MIB_IPNET_ROW2</b> array entry should assume  padding may exist. 



Note that the <i>Netioapi.h</i> header file is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Netioapi.h</i> header file should never be used directly.

## -see-also

<a href="/windows/desktop/api/netioapi/nf-netioapi-getipnettable2">GetIpNetTable2</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipnet_row2">MIB_IPNET_ROW2</a>
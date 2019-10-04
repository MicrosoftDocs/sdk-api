---
UID: NS:netioapi._MIB_MULTICASTIPADDRESS_TABLE
title: MIB_MULTICASTIPADDRESS_TABLE (netioapi.h)
author: windows-sdk-content
description: Contains a table of multicast IP address entries.
old-location: mib\mib_multicastipaddress_table.htm
tech.root: MIB
ms.assetid: 7ae1ec12-aa67-40ff-9641-410099685234
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PMIB_MULTICASTIPADDRESS_TABLE, MIB_MULTICASTIPADDRESS_TABLE, MIB_MULTICASTIPADDRESS_TABLE structure [MIB], PMIB_MULTICASTIPADDRESS_TABLE, PMIB_MULTICASTIPADDRESS_TABLE structure pointer [MIB], _MIB_MULTICASTIPADDRESS_TABLE, mib.mib_multicastipaddress_table, netioapi/MIB_MULTICASTIPADDRESS_TABLE, netioapi/PMIB_MULTICASTIPADDRESS_TABLE"
ms.topic: struct
f1_keywords: 
 - "netioapi/MIB_MULTICASTIPADDRESS_TABLE"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Netioapi.h
api_name:
 - MIB_MULTICASTIPADDRESS_TABLE
targetos: Windows
req.typenames: MIB_MULTICASTIPADDRESS_TABLE, *PMIB_MULTICASTIPADDRESS_TABLE
req.redist: 
ms.custom: 19H1
---

# MIB_MULTICASTIPADDRESS_TABLE structure


## -description


The 
<b>MIB_MULTICASTIPADDRESS_TABLE</b> structure contains a table of multicast IP address entries.


## -struct-fields




### -field NumEntries

A value that specifies the number of multicast IP address entries in the array.


### -field Table

An array of 
<a href="https://docs.microsoft.com/windows/desktop/api/netioapi/ns-netioapi-mib_multicastipaddress_row">MIB_MULTICASTIPADDRESS_ROW</a> structures containing multicast IP address entries.


## -remarks



The <b>MIB_MULTICASTIPADDRESS_TABLE</b> structure is defined on Windows Vista and later. 

The <a href="https://docs.microsoft.com/windows/desktop/api/netioapi/nf-netioapi-getmulticastipaddresstable">GetMulticastIpAddressTable</a> function enumerates the multicast IP addresses on a local system and returns this information in an <b>MIB_MULTICASTIPADDRESS_TABLE</b> structure. 



The <b>MIB_MULTICASTIPADDRESS_TABLE</b> structure may contain padding for alignment between the <b>NumEntries</b> member and the first <a href="https://docs.microsoft.com/windows/desktop/api/netioapi/ns-netioapi-mib_multicastipaddress_row">MIB_MULTICASTIPADDRESS_ROW</a> array entry in the <b>Table</b> member. Padding for alignment may also be present between the <b>MIB_MULTICASTIPADDRESS_ROW</b> array entries in the <b>Table</b> member. Any access to a <b>MIB_MULTICASTIPADDRESS_ROW</b> array entry should assume  padding may exist. 



Note that the <i>Netioapi.h</i> header file is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Netioapi.h</i> header file should never be used directly.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/netioapi/nf-netioapi-getmulticastipaddresstable">GetMulticastIpAddressTable</a>



<a href="https://docs.microsoft.com/windows/desktop/api/netioapi/ns-netioapi-mib_multicastipaddress_row">MIB_MULTICASTIPADDRESS_ROW</a>
 

 


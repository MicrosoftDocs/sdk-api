---
UID: NS:netioapi._MIB_IPFORWARD_TABLE2
title: "_MIB_IPFORWARD_TABLE2"
author: windows-driver-content
description: Contains a table of IP route entries.
old-location: mib\mib_ipforward_table2.htm
old-project: MIB
ms.assetid: 9ba938e8-3395-4c9d-b1d2-b2c030783c16
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: "*PMIB_IPFORWARD_TABLE2, MIB_IPFORWARD_TABLE2, MIB_IPFORWARD_TABLE2 structure [MIB], PMIB_IPFORWARD_TABLE2, PMIB_IPFORWARD_TABLE2 structure pointer [MIB], _MIB_IPFORWARD_TABLE2, mib.mib_ipforward_table2, netioapi/MIB_IPFORWARD_TABLE2, netioapi/PMIB_IPFORWARD_TABLE2"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: MIB_IPFORWARD_TABLE2, *PMIB_IPFORWARD_TABLE2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Netioapi.h
api_name:
-	MIB_IPFORWARD_TABLE2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# _MIB_IPFORWARD_TABLE2 structure


## -description


The 
<b>MIB_IPFORWARD_TABLE2</b> structure contains a table of IP route entries.



## -struct-fields




### -field NumEntries

A value that specifies the number of IP route entries in the array.


### -field Table

An array of 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff559245">MIB_IPFORWARD_ROW2</a> structures containing IP route entries.


## -remarks



The <b>MIB_IPFORWARD_TABLE2</b> structure is defined on Windows Vista and later. 

The <b>GetIpForwardTable2</b> function enumerates the IP route entries on a local system and returns this information in a <b>MIB_IPFORWARD_TABLE2</b> structure. 



The <b>GetIpForwardEntry2</b> function retrieves a single IP route entry and returns this information in a <a href="https://msdn.microsoft.com/library/windows/hardware/ff559245">MIB_IPFORWARD_ROW2</a> structure.

The <b>MIB_IPFORWARD_TABLE2</b> structure may contain padding for alignment between the <b>NumEntries</b> member and the first <a href="https://msdn.microsoft.com/library/windows/hardware/ff559245">MIB_IPFORWARD_ROW2</a> array entry in the <b>Table</b> member. Padding for alignment may also be present between the <b>MIB_IPFORWARD_ROW2</b> array entries in the <b>Table</b> member. Any access to a <b>MIB_IPFORWARD_ROW2</b> array entry should assume  padding may exist. 



Note that the <i>Netioapi.h</i> header file is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Netioapi.h</i> header file should never be used directly.




## -see-also




<b>GetIpForwardEntry2</b>



<b>GetIpForwardTable2</b>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559245">MIB_IPFORWARD_ROW2</a>
 

 


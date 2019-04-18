---
UID: NS:tcpmib._MIB_TCP6TABLE2
title: MIB_TCP6TABLE2 (tcpmib.h)
author: windows-sdk-content
description: Contains a table of IPv6 TCP connections on the local computer.
old-location: mib\mib_tcp6table2.htm
tech.root: MIB
ms.assetid: 3cb8568e-ce31-4ed1-aa9e-abcb826c0cea
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PMIB_TCP6TABLE2, MIB_TCP6TABLE2, MIB_TCP6TABLE2 structure [MIB], PMIB_TCP6TABLE2, PMIB_TCP6TABLE2 structure pointer [MIB], mib.mib_tcp6table2, tcpmib/MIB_TCP6TABLE2, tcpmib/PMIB_TCP6TABLE2"
ms.topic: struct
req.header: tcpmib.h
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
 - Tcpmib.h
api_name:
 - MIB_TCP6TABLE2
product: Windows
targetos: Windows
req.typenames: MIB_TCP6TABLE2, *PMIB_TCP6TABLE2
req.redist: 
ms.custom: 19H1
---

# MIB_TCP6TABLE2 structure


## -description


The 
<b>MIB_TCP6TABLE2</b> structure contains a table of IPv6 TCP connections on the local computer.


## -struct-fields




### -field dwNumEntries

A value that specifies the number of TCP connections in the array.


### -field table

An array of 
<a href="https://msdn.microsoft.com/bbec3397-0317-40f7-926f-2ec48cf5386d">MIB_TCP6ROW2</a> structures containing TCP connection entries.


## -remarks



The <b>MIB_TCP6TABLE2</b> structure is defined on Windows Vista and later. 

The <a href="https://msdn.microsoft.com/435b9198-b921-407c-9441-31cfe77c03f1">GetTcp6Table2</a>function retrieves the IPv6 TCP connection table on the local computer and returns this information in a <b>MIB_TCP6TABLE2</b> structure. 

An array of <a href="https://msdn.microsoft.com/bbec3397-0317-40f7-926f-2ec48cf5386d">MIB_TCP6ROW2</a> structures are contained in the <b>MIB_TCP6TABLE2</b> structure. 

The <b>MIB_TCP6TABLE2</b> structure may contain padding for alignment between the <b>dwNumEntries</b> member and the first <a href="https://msdn.microsoft.com/bbec3397-0317-40f7-926f-2ec48cf5386d">MIB_TCP6ROW2</a> array entry in the <b>table</b> member. Padding for alignment may also be present between the <b>MIB_TCP6ROW2</b> array entries in the <b>table</b> member. Any access to a <b>MIB_TCP6ROW2</b> array entry should assume  padding may exist. 






## -see-also




<a href="https://msdn.microsoft.com/77150609-d06d-4492-bbd7-21eecd825bde">GetTcp6Table</a>



<a href="https://msdn.microsoft.com/435b9198-b921-407c-9441-31cfe77c03f1">GetTcp6Table2</a>



<a href="https://msdn.microsoft.com/e90c5aa0-3126-489b-af44-bf86cb45a6d1">GetTcpTable</a>



<a href="https://msdn.microsoft.com/942e8cb6-545f-45ab-919a-246e3b2d4c6a">GetTcpTable2</a>



<a href="https://msdn.microsoft.com/b3e9eda5-5e86-4790-8b1b-ca9bae44b502">MIB_TCP6ROW</a>



<a href="https://msdn.microsoft.com/bbec3397-0317-40f7-926f-2ec48cf5386d">MIB_TCP6ROW2</a>



<a href="https://msdn.microsoft.com/62bb8544-0a0a-40b5-92cf-9631c9a9987c">MIB_TCP6TABLE</a>



<a href="https://msdn.microsoft.com/36364854-caa8-4652-be8e-f741b36d9fd7">MIB_TCPROW</a>



<a href="https://msdn.microsoft.com/cff343cd-fe85-4e60-87bd-c1e9833cea38">MIB_TCPROW2</a>



<a href="https://msdn.microsoft.com/a8ed8ac2-a72f-4099-ac99-a8b0b77b7b84">MIB_TCPTABLE</a>



<a href="https://msdn.microsoft.com/e07de994-0bd5-4d18-9012-8ff191dd6939">MIB_TCPTABLE2</a>
 

 


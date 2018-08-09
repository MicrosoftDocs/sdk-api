---
UID: NS:udpmib._MIB_UDPTABLE
title: "_MIB_UDPTABLE"
author: windows-sdk-content
description: Contains the User Datagram Protocol (UDP) listener table for IPv4 on the local computer.
old-location: mib\mib_udptable.htm
old-project: mib
ms.assetid: 83608d38-e352-483a-b284-2f9cb444e64f
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: "*PMIB_UDPTABLE, MIB_UDPTABLE, MIB_UDPTABLE structure [MIB], PMIB_UDPTABLE, PMIB_UDPTABLE structure pointer [MIB], _MIB_UDPTABLE, _mpr_mib_udptable, iprtrmib/MIB_UDPTABLE, iprtrmib/PMIB_UDPTABLE, mib.mib_udptable, rras.mib_udptable, udpmib/MIB_UDPTABLE, udpmib/PMIB_UDPTABLE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: udpmib.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MIB_UDPTABLE, *PMIB_UDPTABLE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Udpmib.h
 - Iprtrmib.h
api_name:
 - MIB_UDPTABLE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# _MIB_UDPTABLE structure


## -description


The 
<b>MIB_UDPTABLE</b> structure contains the User Datagram Protocol (UDP)  listener table for IPv4 on the local computer. 


## -struct-fields




### -field dwNumEntries

The number of entries in the table.


### -field table

A pointer to an array of 
<a href="https://msdn.microsoft.com/db366802-962f-4e83-838e-1e2f51beab92">MIB_UDPROW</a> structures.


## -remarks



The <a href="https://msdn.microsoft.com/en-us/library/Aa366033(v=VS.85).aspx">GetUdpTable</a> function enumerates the table of UDP  endpoints for IPv4 that have been bound to an address on the local computer and returns this information in a <b>MIB_UDPTABLE</b> structure. 

This table includes the local IPv4 address and port information for sending and receiving UDP datagrams on the local computer. An array of <a href="https://msdn.microsoft.com/db366802-962f-4e83-838e-1e2f51beab92">MIB_UDPROW</a> structures are contained in the <b>MIB_UDPTABLE</b> structure.

The <b>MIB_UDPTABLE</b> structure may contain padding for alignment between the <b>dwNumEntries</b> member and the first <a href="https://msdn.microsoft.com/db366802-962f-4e83-838e-1e2f51beab92">MIB_UDPROW</a> array entry in the <b>table</b> member. Padding for alignment may also be present between the <b>MIB_UDPROW</b> array entries in the <b>table</b> member. Any access to a <b>MIB_UDPROW</b> array entry should assume  padding may exist. 



The <b>MIB_UDPTABLE</b> structure contains the UDP listener table for IPv4 on the local computer. The name is based on the definition of this table in RFC 1213 published by the IETF. For more information, see 
<a href="http://go.microsoft.com/fwlink/p/?linkid=85984">http://www.ietf.org/rfc/rfc1213.txt</a>. This table contains UDP  endpoints for IPv4 that have been bound to an address. It should be noted that an application can create a UDP socket and bind it to an address for the sole purpose of sending a UDP datagram, with no intention of receiving packets using this socket (functioning as a listener). 

The <a href="https://msdn.microsoft.com/909749d7-a6be-4b3a-b432-79a5aa6e3f4c">MIB_UDPTABLE_OWNER_MODULE</a> structure is an enhanced version of the  <a href="https://msdn.microsoft.com/7c51a1e4-1e07-4fb1-8db3-e48229f12aca">MIB_UDPTABLE_OWNER_PID</a> structure that includes any available ownership data for each UDP endpoint in the table.  The <b>MIB_UDPTABLE_OWNER_PID</b> is an enhanced version of the <b>MIB_UDPTABLE</b> that includes the process ID (PID) that issued the call to the <a href="https://msdn.microsoft.com/3a651daa-7404-4ef7-8cff-0d3dff41a8e8">bind</a> function for each UDP endpoint in the table.

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vistaand later, the organization of header files has changed. This  structure is defined in the <i>Udpmib.h</i> header file, not in the <i>Iprtrmib.h</i> header file. Note that the <i>Udpmib.h</i> header file is automatically included in <i>Iprtrmib.h</i>, which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Udpmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.




## -see-also




<a href="https://msdn.microsoft.com/c936d5a0-ca5e-487e-b304-bfd81403ab40">GetExtendedUdpTable</a>



<a href="https://msdn.microsoft.com/5e86483c-aa39-4d6c-a9b4-9b046b3dcc74">GetUdp6Table</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa366033(v=VS.85).aspx">GetUdpTable</a>



<a href="https://msdn.microsoft.com/c2cc4f77-8557-4206-9e46-aadf065eb8df">MIB_UDP6ROW</a>



<a href="https://msdn.microsoft.com/dcc80b3c-d4d5-44f4-9c7f-df6be2e21889">MIB_UDP6ROW_OWNER_MODULE</a>



<a href="https://msdn.microsoft.com/d3d02485-381b-4058-b4b9-0a2c9c365f43">MIB_UDP6ROW_OWNER_PID</a>



<a href="https://msdn.microsoft.com/49da9a1f-f244-464e-96b2-944a286445d4">MIB_UDP6TABLE</a>



<a href="https://msdn.microsoft.com/11bf2d6d-b9bc-4a4d-b7b0-6f7d61eb3756">MIB_UDP6TABLE_OWNER_MODULE</a>



<a href="https://msdn.microsoft.com/6c8d1cb9-209b-47a0-b41c-6b4098a4a81e">MIB_UDP6TABLE_OWNER_PID</a>



<a href="https://msdn.microsoft.com/db366802-962f-4e83-838e-1e2f51beab92">MIB_UDPROW</a>



<a href="https://msdn.microsoft.com/9ae304e0-4653-4757-a823-d4ccf68627bf">MIB_UDPROW_OWNER_MODULE</a>



<a href="https://msdn.microsoft.com/b914b6eb-adf9-4a61-ae8f-05d3ff90ce90">MIB_UDPROW_OWNER_PID</a>



<a href="https://msdn.microsoft.com/909749d7-a6be-4b3a-b432-79a5aa6e3f4c">MIB_UDPTABLE_OWNER_MODULE</a>



<a href="https://msdn.microsoft.com/7c51a1e4-1e07-4fb1-8db3-e48229f12aca">MIB_UDPTABLE_OWNER_PID</a>



<a href="https://msdn.microsoft.com/3a651daa-7404-4ef7-8cff-0d3dff41a8e8">bind</a>
 

 


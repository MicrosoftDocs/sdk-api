---
UID: NE:iprtrmib._UDP_TABLE_CLASS
title: "_UDP_TABLE_CLASS"
author: windows-sdk-content
description: Defines the set of values used to indicate the type of table returned by calls to GetExtendedUdpTable.
old-location: iphlp\udp_table_class.htm
old-project: IpHlp
ms.assetid: 2e7304d1-b89c-46d4-9121-936a1c38cc51
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: "*PUDP_TABLE_CLASS, PUDP_TABLE_CLASS, PUDP_TABLE_CLASS enumeration pointer [IP Helper], UDP_TABLE_BASIC, UDP_TABLE_CLASS, UDP_TABLE_CLASS enumeration [IP Helper], UDP_TABLE_OWNER_MODULE, UDP_TABLE_OWNER_PID, _UDP_TABLE_CLASS, iphlp.udp_table_class, iphlpapi/PUDP_TABLE_CLASS, iphlpapi/UDP_TABLE_BASIC, iphlpapi/UDP_TABLE_CLASS, iphlpapi/UDP_TABLE_OWNER_MODULE, iphlpapi/UDP_TABLE_OWNER_PID, iprtrmib/PUDP_TABLE_CLASS, iprtrmib/UDP_TABLE_BASIC, iprtrmib/UDP_TABLE_CLASS, iprtrmib/UDP_TABLE_OWNER_MODULE, iprtrmib/UDP_TABLE_OWNER_PID"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: iprtrmib.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
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
req.typenames: UDP_TABLE_CLASS, *PUDP_TABLE_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Iprtrmib.h
-	Iphlpapi.h
api_name:
-	UDP_TABLE_CLASS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _UDP_TABLE_CLASS enumeration


## -description


The <b>UDP_TABLE_CLASS</b> enumeration defines the set of values used to  indicate the type of table returned by calls to <a href="https://msdn.microsoft.com/c936d5a0-ca5e-487e-b304-bfd81403ab40">GetExtendedUdpTable</a>.


## -enum-fields




### -field UDP_TABLE_BASIC

A <a href="https://msdn.microsoft.com/83608d38-e352-483a-b284-2f9cb444e64f">MIB_UDPTABLE</a> structure that contains all UDP endpoints on the local computer is returned to the caller.


### -field UDP_TABLE_OWNER_PID

A <a href="https://msdn.microsoft.com/7c51a1e4-1e07-4fb1-8db3-e48229f12aca">MIB_UDPTABLE_OWNER_PID</a> or <a href="https://msdn.microsoft.com/6c8d1cb9-209b-47a0-b41c-6b4098a4a81e">MIB_UDP6TABLE_OWNER_PID</a> structure that contains all UDP endpoints on the local computer is returned to the caller.


### -field UDP_TABLE_OWNER_MODULE

A <a href="https://msdn.microsoft.com/909749d7-a6be-4b3a-b432-79a5aa6e3f4c">MIB_UDPTABLE_OWNER_MODULE</a> or <a href="https://msdn.microsoft.com/11bf2d6d-b9bc-4a4d-b7b0-6f7d61eb3756">MIB_UDP6TABLE_OWNER_MODULE</a> structure that contains all  UDP endpoints on the local computer is returned to the caller.


## -remarks



On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <b>UDP_TABLE_CLASS</b> enumeration  is defined in the <i>Iprtrmib.h</i> header file, not in the <i>Iphlpapi.h</i> header file. Note that the <i>Iprtrmib.h</i> header file is automatically included in <i>Iphlpapi.h</i> header file. The <i>Iprtrmib.h</i> header files should never be used directly.






## -see-also




<a href="https://msdn.microsoft.com/c936d5a0-ca5e-487e-b304-bfd81403ab40">GetExtendedUdpTable</a>
 

 


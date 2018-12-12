---
UID: NS:netioapi._MIB_IFSTACK_TABLE
title: MIB_IFSTACK_TABLE
author: windows-sdk-content
description: Contains a table of network interface stack row entries. This specifies the relationship of the network interfaces on an interface stack.
old-location: mib\mib_ifstack_table.htm
tech.root: MIB
ms.assetid: b2f6eea7-c3d4-493d-bf55-bc95b97601bd
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PMIB_IFSTACK_TABLE, MIB_IFSTACK_TABLE, MIB_IFSTACK_TABLE structure [MIB], PMIB_IFSTACK_TABLE, PMIB_IFSTACK_TABLE structure pointer [MIB], _MIB_IFSTACK_TABLE, mib.mib_ifstack_table, netioapi/MIB_IFSTACK_TABLE, netioapi/PMIB_IFSTACK_TABLE"
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
 - MIB_IFSTACK_TABLE
product: Windows
targetos: Windows
req.typenames: MIB_IFSTACK_TABLE, *PMIB_IFSTACK_TABLE
req.redist: 
---

# MIB_IFSTACK_TABLE structure


## -description


The 
<b>MIB_IFSTACK_TABLE</b> structure contains a table of network interface stack row entries. This  specifies the relationship of the network interfaces on an interface stack.


## -struct-fields




### -field NumEntries

The number of interface stack row entries in the array.


### -field Table

An array of 
<a href="https://msdn.microsoft.com/f86dfb52-98e8-4725-990c-5de788bebef1">MIB_IFSTACK_ROW</a> structures containing interface stack row entries.


## -remarks



The <b>MIB_IFSTACK_TABLE</b> structure is defined in Windows Vista and later. 

The relationship between the interfaces in the interface stack is that the interface with index in the <b>HigherLayerInterfaceIndex</b> member of the <a href="https://msdn.microsoft.com/f86dfb52-98e8-4725-990c-5de788bebef1">MIB_IFSTACK_ROW</a> structure is immediately above the interface with index in the <b>LowerLayerInterfaceIndex</b> member of the <b>MIB_IFSTACK_ROW</b> structure.

The <a href="https://msdn.microsoft.com/c1b0f091-2aef-447e-9866-a886838a6267">GetIfStackTable</a> function enumerates the network interface stack row entries on a local system and returns this information in a <b>MIB_IFSTACK_TABLE</b> structure. 



The <b>MIB_IFSTACK_TABLE</b> structure may contain padding for alignment between the <b>NumEntries</b> member and the first <a href="https://msdn.microsoft.com/f86dfb52-98e8-4725-990c-5de788bebef1">MIB_IFSTACK_ROW</a> array entry in the <b>Table</b> member. Padding for alignment may also be present between the <b>MIB_IFSTACK_ROW</b> array entries in the <b>Table</b> member. Any access to a <b>MIB_IFSTACK_ROW</b> array entry should assume  padding may exist. 



Note that the <i>Netioapi.h</i> header file is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Netioapi.h</i> header file should never be used directly.




## -see-also




<a href="https://msdn.microsoft.com/c1b0f091-2aef-447e-9866-a886838a6267">GetIfStackTable</a>



<a href="https://msdn.microsoft.com/d1808ded-2798-46cc-8021-fdbcd3da60ea">GetInvertedIfStackTable</a>



<a href="https://msdn.microsoft.com/f86dfb52-98e8-4725-990c-5de788bebef1">MIB_IFSTACK_ROW</a>



<a href="https://msdn.microsoft.com/dedccd32-b922-4729-92f3-879e98a7dc7a">MIB_INVERTEDIFSTACK_ROW</a>



<a href="https://msdn.microsoft.com/b3508bb5-4e36-4088-afcc-4a75a01d1fe6">MIB_INVERTEDIFSTACK_TABLE</a>
 

 


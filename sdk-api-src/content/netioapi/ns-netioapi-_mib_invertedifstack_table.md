---
UID: NS:netioapi._MIB_INVERTEDIFSTACK_TABLE
title: "_MIB_INVERTEDIFSTACK_TABLE"
author: windows-sdk-content
description: Contains a table of inverted network interface stack row entries. This specifies the relationship of the network interfaces on an interface stack in reverse order.
old-location: mib\mib_invertedifstack_table.htm
old-project: mib
ms.assetid: b3508bb5-4e36-4088-afcc-4a75a01d1fe6
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: "*PMIB_INVERTEDIFSTACK_TABLE, MIB_INVERTEDIFSTACK_TABLE, MIB_INVERTEDIFSTACK_TABLE structure [MIB], PMIB_INVERTEDIFSTACK_TABLE, PMIB_INVERTEDIFSTACK_TABLE structure pointer [MIB], _MIB_INVERTEDIFSTACK_TABLE, mib.mib_invertedifstack_table, netioapi/MIB_INVERTEDIFSTACK_TABLE, netioapi/PMIB_INVERTEDIFSTACK_TABLE"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MIB_INVERTEDIFSTACK_TABLE, *PMIB_INVERTEDIFSTACK_TABLE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Netioapi.h
api_name:
 - MIB_INVERTEDIFSTACK_TABLE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _MIB_INVERTEDIFSTACK_TABLE structure


## -description


The 
<b>MIB_INVERTEDIFSTACK_TABLE</b> structure contains a table of inverted network interface stack row entries. This  specifies the relationship of the network interfaces on an interface stack in reverse order.


## -struct-fields




### -field NumEntries

The number of inverted interface stack row entries in the array.


### -field Table

An array of 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff559234">MIB_INVERTEDIFSTACK_ROW</a> structures containing inverted interface stack row entries.


## -remarks



The <b>MIB_INVERTEDIFSTACK_TABLE</b> structure is defined on Windows Vista and later. 

The relationship between the interfaces in the interface stack is that the interface with index in the <b>HigherLayerInterfaceIndex</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559234">MIB_INVERTEDIFSTACK_ROW</a> structure is immediately above the interface with index in the <b>LowerLayerInterfaceIndex</b> member of the <b>MIB_INVERTEDIFSTACK_ROW</b> structure.

The <a href="https://msdn.microsoft.com/library/windows/hardware/ff552531">GetInvertedIfStackTable</a> function enumerates the inverted network interface stack row entries on a local system and returns this information in a <b>MIB_INVERTEDIFSTACK_TABLE</b> structure. 



The <b>MIB_INVERTEDIFSTACK_TABLE</b> structure may contain padding for alignment between the <b>NumEntries</b> member and the first <a href="https://msdn.microsoft.com/library/windows/hardware/ff559234">MIB_INVERTEDIFSTACK_ROW</a> array entry in the <b>Table</b> member. Padding for alignment may also be present between the <b>MIB_INVERTEDIFSTACK_ROW</b> array entries in the <b>Table</b> member. Any access to a <b>MIB_INVERTEDIFSTACK_ROW</b> array entry should assume  padding may exist. 



Note that the <i>Netioapi.h</i> header file is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Netioapi.h</i> header file should never be used directly.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552521">GetIfStackTable</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552531">GetInvertedIfStackTable</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559207">MIB_IFSTACK_ROW</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559210">MIB_IFSTACK_TABLE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559234">MIB_INVERTEDIFSTACK_ROW</a>
 

 


---
UID: NS:netioapi._MIB_IFSTACK_ROW
title: MIB_IFSTACK_ROW
author: windows-sdk-content
description: Represents the relationship between two network interfaces.
old-location: mib\mib_ifstack_row.htm
tech.root: MIB
ms.assetid: f86dfb52-98e8-4725-990c-5de788bebef1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PMIB_IFSTACK_ROW, MIB_IFSTACK_ROW, MIB_IFSTACK_ROW structure [MIB], PMIB_IFSTACK_ROW, PMIB_IFSTACK_ROW structure pointer [MIB], _MIB_IFSTACK_ROW, mib.mib_ifstack_row, netioapi/MIB_IFSTACK_ROW, netioapi/PMIB_IFSTACK_ROW"
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
 - MIB_IFSTACK_ROW
product: Windows
targetos: Windows
req.typenames: MIB_IFSTACK_ROW, *PMIB_IFSTACK_ROW
req.redist: 
---

# MIB_IFSTACK_ROW structure


## -description


The 
<b>MIB_IFSTACK_ROW</b> structure represents the relationship between two network interfaces.


## -struct-fields




### -field HigherLayerInterfaceIndex

The network interface index for the interface that is higher in the interface stack table.


### -field LowerLayerInterfaceIndex

The network interface index for the interface that is lower in the interface stack table.


## -remarks



The <b>MIB_IFSTACK_ROW</b> structure is defined in Windows Vista and later. 

The relationship between the interfaces in the interface stack is that the interface with index in the <b>HigherLayerInterfaceIndex</b> member is immediately above the interface with index in the <b>LowerLayerInterfaceIndex</b> member.

Note that the <i>Netioapi.h</i> header file is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Netioapi.h</i> header file should never be used directly.




## -see-also




<a href="https://msdn.microsoft.com/c1b0f091-2aef-447e-9866-a886838a6267">GetIfStackTable</a>



<a href="https://msdn.microsoft.com/d1808ded-2798-46cc-8021-fdbcd3da60ea">GetInvertedIfStackTable</a>



<a href="https://msdn.microsoft.com/b2f6eea7-c3d4-493d-bf55-bc95b97601bd">MIB_IFSTACK_TABLE</a>



<a href="https://msdn.microsoft.com/dedccd32-b922-4729-92f3-879e98a7dc7a">MIB_INVERTEDIFSTACK_ROW</a>



<a href="https://msdn.microsoft.com/b3508bb5-4e36-4088-afcc-4a75a01d1fe6">MIB_INVERTEDIFSTACK_TABLE</a>
 

 


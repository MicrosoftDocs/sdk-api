---
UID: NS:netioapi._MIB_IFSTACK_ROW
title: "_MIB_IFSTACK_ROW"
author: windows-sdk-content
description: Represents the relationship between two network interfaces.
old-location: mib\mib_ifstack_row.htm
old-project: MIB
ms.assetid: f86dfb52-98e8-4725-990c-5de788bebef1
ms.author: windowssdkdev
ms.date: 05/14/2018
ms.keywords: "*PMIB_IFSTACK_ROW, MIB_IFSTACK_ROW, MIB_IFSTACK_ROW structure [MIB], PMIB_IFSTACK_ROW, PMIB_IFSTACK_ROW structure pointer [MIB], _MIB_IFSTACK_ROW, mib.mib_ifstack_row, netioapi/MIB_IFSTACK_ROW, netioapi/PMIB_IFSTACK_ROW"
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
req.typenames: MIB_IFSTACK_ROW, *PMIB_IFSTACK_ROW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Netioapi.h
api_name:
-	MIB_IFSTACK_ROW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _MIB_IFSTACK_ROW structure


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




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552521">GetIfStackTable</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552531">GetInvertedIfStackTable</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559210">MIB_IFSTACK_TABLE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559234">MIB_INVERTEDIFSTACK_ROW</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559240">MIB_INVERTEDIFSTACK_TABLE</a>
 

 


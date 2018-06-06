---
UID: NE:netioapi._MIB_IF_TABLE_LEVEL
title: "_MIB_IF_TABLE_LEVEL"
author: windows-sdk-content
description: The MIB_IF_TABLE_LEVEL enumeration type defines the level of interface information to retrieve.
old-location: netvista\mib_if_table_level.htm
old-project: netvista
ms.assetid: ffbde22e-9851-4acd-b820-b71f2788b4d2
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: "*PMIB_IF_TABLE_LEVEL, MIB_IF_TABLE_LEVEL, MIB_IF_TABLE_LEVEL enumeration [Network Drivers Starting with Windows Vista], MibIfTableNormal, MibIfTableNormalWithoutStatistics, MibIfTableRaw, PMIB_IF_TABLE_LEVEL, PMIB_IF_TABLE_LEVEL enumeration pointer [Network Drivers Starting with Windows Vista], _MIB_IF_TABLE_LEVEL, _MIB_IF_TABLE_LEVEL enumeration [Network Drivers Starting with Windows Vista], iphelper_5f6cb0fa-b27b-45b6-882c-bb9852020775.xml, netioapi/MibIfTableNormal, netioapi/MibIfTableNormalWithoutStatistics, netioapi/MibIfTableRaw, netioapi/PMIB_IF_TABLE_LEVEL, netioapi/_MIB_IF_TABLE_LEVEL, netvista.mib_if_table_level"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: netioapi.h
req.include-header: Netioapi.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows Vista and later versions of the Windows operating   systems.
req.target-min-winversvr: 
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
req.typenames: MIB_IF_TABLE_LEVEL, *PMIB_IF_TABLE_LEVEL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - netioapi.h
api_name:
 - MIB_IF_TABLE_LEVEL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _MIB_IF_TABLE_LEVEL enumeration


## -description


The MIB_IF_TABLE_LEVEL enumeration type defines the level of interface information to
  retrieve.


## -enum-fields




### -field MibIfTableNormal

The values of statistics and state that are returned in members of the 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff559214">MIB_IF_ROW2</a> structure in the 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff559224">MIB_IF_TABLE2</a> structure that the 
     <i>Table</i> parameter points to in the 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff552528">GetIfTable2Ex</a> function are returned from
     the top of the filter stack.


### -field MibIfTableRaw

The values of statistics and state that are returned in members of the 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff559214">MIB_IF_ROW2</a> structure in the 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff559224">MIB_IF_TABLE2</a> structure that the 
     <i>Table</i> parameter points to in the 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff552528">GetIfTable2Ex</a> function are returned
     directly for the interface that is being queried.


### -field MibIfTableNormalWithoutStatistics

<div class="alert"><b>Note</b>  This value is available starting with Windows 10, version 1703.</div>
<div> </div>
The values returned are the same as for the <b>MibIfTableNormal </b> value, but without the statistics.


## -remarks



The MIB_IF_TABLE_LEVEL enumeration type is used with the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff552528">GetIfTable2Ex</a> function to specify the level
    of interface information to retrieve.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552528">GetIfTable2Ex</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559214">MIB_IF_ROW2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559224">MIB_IF_TABLE2</a>
 

 


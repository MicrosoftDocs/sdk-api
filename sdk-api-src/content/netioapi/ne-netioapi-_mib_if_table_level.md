---
UID: NE:netioapi._MIB_IF_TABLE_LEVEL
title: "_MIB_IF_TABLE_LEVEL"
author: windows-sdk-content
description: The MIB_IF_TABLE_LEVEL enumeration type defines the level of interface information to retrieve.
old-location: netvista\mib_if_table_level.htm
tech.root: NetVista
ms.assetid: ffbde22e-9851-4acd-b820-b71f2788b4d2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PMIB_IF_TABLE_LEVEL, MIB_IF_TABLE_LEVEL, MIB_IF_TABLE_LEVEL enumeration [Network Drivers Starting with Windows Vista], MibIfTableNormal, MibIfTableNormalWithoutStatistics, MibIfTableRaw, PMIB_IF_TABLE_LEVEL, PMIB_IF_TABLE_LEVEL enumeration pointer [Network Drivers Starting with Windows Vista], _MIB_IF_TABLE_LEVEL, _MIB_IF_TABLE_LEVEL enumeration [Network Drivers Starting with Windows Vista], iphelper_5f6cb0fa-b27b-45b6-882c-bb9852020775.xml, netioapi/MibIfTableNormal, netioapi/MibIfTableNormalWithoutStatistics, netioapi/MibIfTableRaw, netioapi/PMIB_IF_TABLE_LEVEL, netioapi/_MIB_IF_TABLE_LEVEL, netvista.mib_if_table_level"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: MIB_IF_TABLE_LEVEL, *PMIB_IF_TABLE_LEVEL
req.redist: 
---

# _MIB_IF_TABLE_LEVEL enumeration


## -description


The MIB_IF_TABLE_LEVEL enumeration type defines the level of interface information to
  retrieve.


## -enum-fields




### -field MibIfTableNormal

The values of statistics and state that are returned in members of the 
     <a href="https://msdn.microsoft.com/37d5fc98-7d56-4f34-9806-8c0de69835a1">MIB_IF_ROW2</a> structure in the 
     <a href="https://msdn.microsoft.com/9df0cd0a-6d94-4a4b-8035-0f94b1cfa247">MIB_IF_TABLE2</a> structure that the 
     <i>Table</i> parameter points to in the 
     <a href="https://msdn.microsoft.com/d7bcedc0-3bf2-48f7-9e6f-6a0224b0ce26">GetIfTable2Ex</a> function are returned from
     the top of the filter stack.


### -field MibIfTableRaw

The values of statistics and state that are returned in members of the 
     <a href="https://msdn.microsoft.com/37d5fc98-7d56-4f34-9806-8c0de69835a1">MIB_IF_ROW2</a> structure in the 
     <a href="https://msdn.microsoft.com/9df0cd0a-6d94-4a4b-8035-0f94b1cfa247">MIB_IF_TABLE2</a> structure that the 
     <i>Table</i> parameter points to in the 
     <a href="https://msdn.microsoft.com/d7bcedc0-3bf2-48f7-9e6f-6a0224b0ce26">GetIfTable2Ex</a> function are returned
     directly for the interface that is being queried.


### -field MibIfTableNormalWithoutStatistics

<div class="alert"><b>Note</b>  This value is available starting with Windows 10, version 1703.</div>
<div> </div>
The values returned are the same as for the <b>MibIfTableNormal </b> value, but without the statistics.


## -remarks



The MIB_IF_TABLE_LEVEL enumeration type is used with the 
    <a href="https://msdn.microsoft.com/d7bcedc0-3bf2-48f7-9e6f-6a0224b0ce26">GetIfTable2Ex</a> function to specify the level
    of interface information to retrieve.




## -see-also




<a href="https://msdn.microsoft.com/d7bcedc0-3bf2-48f7-9e6f-6a0224b0ce26">GetIfTable2Ex</a>



<a href="https://msdn.microsoft.com/37d5fc98-7d56-4f34-9806-8c0de69835a1">MIB_IF_ROW2</a>



<a href="https://msdn.microsoft.com/9df0cd0a-6d94-4a4b-8035-0f94b1cfa247">MIB_IF_TABLE2</a>
 

 


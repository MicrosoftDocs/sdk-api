---
UID: NE:netioapi._MIB_IF_TABLE_LEVEL
title: MIB_IF_TABLE_LEVEL (netioapi.h)
description: The MIB_IF_TABLE_LEVEL enumeration type defines the level of interface information to retrieve.
helpviewer_keywords: ["*PMIB_IF_TABLE_LEVEL","MIB_IF_TABLE_LEVEL","MIB_IF_TABLE_LEVEL enumeration [Network Drivers Starting with Windows Vista]","MibIfTableNormal","MibIfTableNormalWithoutStatistics","MibIfTableRaw","PMIB_IF_TABLE_LEVEL","PMIB_IF_TABLE_LEVEL enumeration pointer [Network Drivers Starting with Windows Vista]","_MIB_IF_TABLE_LEVEL","_MIB_IF_TABLE_LEVEL enumeration [Network Drivers Starting with Windows Vista]","iphelper_5f6cb0fa-b27b-45b6-882c-bb9852020775.xml","netioapi/MibIfTableNormal","netioapi/MibIfTableNormalWithoutStatistics","netioapi/MibIfTableRaw","netioapi/PMIB_IF_TABLE_LEVEL","netioapi/_MIB_IF_TABLE_LEVEL","netvista.mib_if_table_level"]
old-location: netvista\mib_if_table_level.htm
tech.root: NetVista
ms.assetid: ffbde22e-9851-4acd-b820-b71f2788b4d2
ms.date: 12/05/2018
ms.keywords: '*PMIB_IF_TABLE_LEVEL, MIB_IF_TABLE_LEVEL, MIB_IF_TABLE_LEVEL enumeration [Network Drivers Starting with Windows Vista], MibIfTableNormal, MibIfTableNormalWithoutStatistics, MibIfTableRaw, PMIB_IF_TABLE_LEVEL, PMIB_IF_TABLE_LEVEL enumeration pointer [Network Drivers Starting with Windows Vista], _MIB_IF_TABLE_LEVEL, _MIB_IF_TABLE_LEVEL enumeration [Network Drivers Starting with Windows Vista], iphelper_5f6cb0fa-b27b-45b6-882c-bb9852020775.xml, netioapi/MibIfTableNormal, netioapi/MibIfTableNormalWithoutStatistics, netioapi/MibIfTableRaw, netioapi/PMIB_IF_TABLE_LEVEL, netioapi/_MIB_IF_TABLE_LEVEL, netvista.mib_if_table_level'
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
targetos: Windows
req.typenames: MIB_IF_TABLE_LEVEL, *PMIB_IF_TABLE_LEVEL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_IF_TABLE_LEVEL
 - netioapi/_MIB_IF_TABLE_LEVEL
 - PMIB_IF_TABLE_LEVEL
 - netioapi/PMIB_IF_TABLE_LEVEL
 - MIB_IF_TABLE_LEVEL
 - netioapi/MIB_IF_TABLE_LEVEL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - netioapi.h
api_name:
 - MIB_IF_TABLE_LEVEL
---

# MIB_IF_TABLE_LEVEL enumeration


## -description

The MIB_IF_TABLE_LEVEL enumeration type defines the level of interface information to
  retrieve.

## -enum-fields

### -field MibIfTableNormal

The values of statistics and state that are returned in members of the 
     <a href="/previous-versions/windows/hardware/drivers/ff559214(v=vs.85)">MIB_IF_ROW2</a> structure in the 
     <a href="/previous-versions/windows/hardware/drivers/ff559224(v=vs.85)">MIB_IF_TABLE2</a> structure that the 
     <i>Table</i> parameter points to in the 
     <a href="/previous-versions/windows/hardware/drivers/ff552528(v=vs.85)">GetIfTable2Ex</a> function are returned from
     the top of the filter stack.

### -field MibIfTableRaw

The values of statistics and state that are returned in members of the 
     <a href="/previous-versions/windows/hardware/drivers/ff559214(v=vs.85)">MIB_IF_ROW2</a> structure in the 
     <a href="/previous-versions/windows/hardware/drivers/ff559224(v=vs.85)">MIB_IF_TABLE2</a> structure that the 
     <i>Table</i> parameter points to in the 
     <a href="/previous-versions/windows/hardware/drivers/ff552528(v=vs.85)">GetIfTable2Ex</a> function are returned
     directly for the interface that is being queried.

### -field MibIfTableNormalWithoutStatistics

<div class="alert"><b>Note</b>  This value is available starting with Windows 10, version 1703.</div>
<div> </div>
The values returned are the same as for the <b>MibIfTableNormal </b> value, but without the statistics.

## -remarks

The MIB_IF_TABLE_LEVEL enumeration type is used with the 
    <a href="/previous-versions/windows/hardware/drivers/ff552528(v=vs.85)">GetIfTable2Ex</a> function to specify the level
    of interface information to retrieve.

## -see-also

<a href="/previous-versions/windows/hardware/drivers/ff552528(v=vs.85)">GetIfTable2Ex</a>



<a href="/previous-versions/windows/hardware/drivers/ff559214(v=vs.85)">MIB_IF_ROW2</a>



<a href="/previous-versions/windows/hardware/drivers/ff559224(v=vs.85)">MIB_IF_TABLE2</a>
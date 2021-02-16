---
UID: NS:iprtrmib._MIB_IFSTATUS
title: MIB_IFSTATUS (iprtrmib.h)
description: Stores status information for a particular interface.
helpviewer_keywords: ["*PMIB_IFSTATUS","MIB_IFSTATUS","MIB_IFSTATUS structure [MIB]","PMIB_IFSTATUS","PMIB_IFSTATUS structure pointer [MIB]","_mpr_mib_ifstatus","iprtrmib/MIB_IFSTATUS","iprtrmib/PMIB_IFSTATUS","mib.mib_ifstatus","rras.mib_ifstatus"]
old-location: mib\mib_ifstatus.htm
tech.root: MIB
ms.assetid: ab5afe84-1e14-4ffd-9bf6-f3b319554608
ms.date: 12/05/2018
ms.keywords: '*PMIB_IFSTATUS, MIB_IFSTATUS, MIB_IFSTATUS structure [MIB], PMIB_IFSTATUS, PMIB_IFSTATUS structure pointer [MIB], _mpr_mib_ifstatus, iprtrmib/MIB_IFSTATUS, iprtrmib/PMIB_IFSTATUS, mib.mib_ifstatus, rras.mib_ifstatus'
req.header: iprtrmib.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MIB_IFSTATUS, *PMIB_IFSTATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_IFSTATUS
 - iprtrmib/_MIB_IFSTATUS
 - PMIB_IFSTATUS
 - iprtrmib/PMIB_IFSTATUS
 - MIB_IFSTATUS
 - iprtrmib/MIB_IFSTATUS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iprtrmib.h
api_name:
 - MIB_IFSTATUS
---

# MIB_IFSTATUS structure


## -description

The 
<b>MIB_IFSTATUS</b> structure stores status information for a particular interface.

## -struct-fields

### -field dwIfIndex

The index that identifies the interface.

### -field dwAdminStatus

The administrative status of the interface, that is, whether the interface is administratively enabled or disabled.

### -field dwOperationalStatus

The operational status of the interface. This member can be one of the values defined in the <a href="/windows/desktop/api/mprapi/ne-mprapi-router_connection_state">ROUTER_CONNECTION_STATE</a> enumeration defined in the <i>Mprapip.h</i> header file. See 
the <b>ROUTER_CONNECTION_STATE</b> enumeration for a list amd description of the possible operational states.

### -field bMHbeatActive

Specifies whether multicast heartbeat detection is enabled. A value of <b>TRUE</b> indicates that heartbeat detection is enabled. A value of <b>FALSE</b> indicates that heartbeat detection is disabled.

### -field bMHbeatAlive

Specifies whether the multicast heartbeat dead interval has been exceeded. A value of <b>FALSE</b> indicates that the interval has been exceeded. A value of <b>TRUE</b> indicates that the interval has not been exceeded.

## -remarks

Note that the <i>Iprtrmib.h</i> header file is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Iprtrmib.h</i> header file should never be used directly.

## -see-also

<a href="/windows/desktop/api/ifmib/ns-ifmib-mib_ifrow">MIB_IFROW</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_interface_0">MPR_INTERFACE_0</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_interface_1">MPR_INTERFACE_1</a>
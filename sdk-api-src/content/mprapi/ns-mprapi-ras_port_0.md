---
UID: NS:mprapi._RAS_PORT_0
title: RAS_PORT_0 (mprapi.h)
description: The RAS_PORT_0 structure contains general information regarding a specific RAS port, such as port condition and port name. For more detailed information about a specific port, such as line speed or errors, see RAS_PORT_1.
helpviewer_keywords: ["*PRAS_PORT_0","PRAS_PORT_0","PRAS_PORT_0 structure pointer [RAS]","RAS_PORT_0","RAS_PORT_0 structure [RAS]","_mpr_ras_port_0","mprapi/PRAS_PORT_0","mprapi/RAS_PORT_0","rras.ras_port_0"]
old-location: rras\ras_port_0.htm
tech.root: RRAS
ms.assetid: 361b065e-8240-465f-a0fe-d4bfc097ec70
ms.date: 12/05/2018
ms.keywords: '*PRAS_PORT_0, PRAS_PORT_0, PRAS_PORT_0 structure pointer [RAS], RAS_PORT_0, RAS_PORT_0 structure [RAS], _mpr_ras_port_0, mprapi/PRAS_PORT_0, mprapi/RAS_PORT_0, rras.ras_port_0'
req.header: mprapi.h
req.include-header: 
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
req.typenames: RAS_PORT_0, *PRAS_PORT_0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RAS_PORT_0
 - mprapi/_RAS_PORT_0
 - PRAS_PORT_0
 - mprapi/PRAS_PORT_0
 - RAS_PORT_0
 - mprapi/RAS_PORT_0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mprapi.h
api_name:
 - RAS_PORT_0
---

# RAS_PORT_0 structure


## -description

The 
<b>RAS_PORT_0</b> structure contains general information regarding a specific RAS port, such as port condition and port name. For more detailed information about a specific port, such as line speed or errors, see 
<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_port_1">RAS_PORT_1</a>.

## -struct-fields

### -field hPort

Handle to the port.

### -field hConnection

Handle to the connection.

### -field dwPortCondition

<a href="/windows/desktop/api/mprapi/ne-mprapi-ras_port_condition">RAS_PORT_CONDITION</a> structure.

### -field dwTotalNumberOfCalls

Specifies the cumulative number of calls this port has serviced.

### -field dwConnectDuration

Specifies the duration of the current connection, in seconds.

### -field wszPortName

Specifies the port name.

### -field wszMediaName

Specifies the media name.

### -field wszDeviceName

Specifies the device name.

### -field wszDeviceType

Specifies the device type.

## -see-also

<a href="/windows/desktop/RRAS/ras-administration-structures">RAS
		  Administration Structures</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_port_1">RAS_PORT_1</a>



<a href="/windows/desktop/api/mprapi/ne-mprapi-ras_port_condition">RAS_PORT_CONDITION</a>



<a href="/windows/desktop/RRAS/remote-access-service-administration-reference">Remote Access Service Administration Reference</a>
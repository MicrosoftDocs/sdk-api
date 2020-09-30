---
UID: NS:mprapi._RAS_PORT_1
title: RAS_PORT_1 (mprapi.h)
description: The RAS_PORT_1 structure contains detailed information regarding a specific RAS port, such as line speed or errors. For more general information about a port, such as port condition or port name, see RAS_PORT_0.
helpviewer_keywords: ["*PRAS_PORT_1","PRAS_PORT_1","PRAS_PORT_1 structure pointer [RAS]","RAS_PORT_1","RAS_PORT_1 structure [RAS]","_mpr_ras_port_1","mprapi/PRAS_PORT_1","mprapi/RAS_PORT_1","rras.ras_port_1"]
old-location: rras\ras_port_1.htm
tech.root: RRAS
ms.assetid: 4850f08e-13ee-485f-99a5-be4554d6311b
ms.date: 12/05/2018
ms.keywords: '*PRAS_PORT_1, PRAS_PORT_1, PRAS_PORT_1 structure pointer [RAS], RAS_PORT_1, RAS_PORT_1 structure [RAS], _mpr_ras_port_1, mprapi/PRAS_PORT_1, mprapi/RAS_PORT_1, rras.ras_port_1'
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
req.typenames: RAS_PORT_1, *PRAS_PORT_1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RAS_PORT_1
 - mprapi/_RAS_PORT_1
 - PRAS_PORT_1
 - mprapi/PRAS_PORT_1
 - RAS_PORT_1
 - mprapi/RAS_PORT_1
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
 - RAS_PORT_1
---

# RAS_PORT_1 structure


## -description

The 
<b>RAS_PORT_1</b> structure contains detailed information regarding a specific RAS port, such as line speed or errors. For more general information about a port, such as port condition or port name, see 
<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_port_0">RAS_PORT_0</a>.

## -struct-fields

### -field hPort

Handle to the port.

### -field hConnection

Handle to the connection.

### -field dwHardwareCondition

Specifies a 
<a href="/windows/desktop/api/mprapi/ne-mprapi-ras_hardware_condition">RAS_HARDWARE_CONDITION</a> structure.

### -field dwLineSpeed

Specifies the line speed of the port, represented in bits per second.

### -field dwBytesXmited

Specifies the bytes transmitted on the port. This value is the number of bytes of compressed data.

### -field dwBytesRcved

Specifies the bytes received on the port. This value is the number of bytes of compressed data.

### -field dwFramesXmited

Specifies the frames transmitted on the port.

### -field dwFramesRcved

Specifies the frames received on the port.

### -field dwCrcErr

Specifies the CRC errors on the port.

### -field dwTimeoutErr

Specifies the time-out errors on the port.

### -field dwAlignmentErr

Specifies the alignment errors on the port.

### -field dwHardwareOverrunErr

Specifies the hardware overrun errors on the port.

### -field dwFramingErr

Specifies the framing errors on the port.

### -field dwBufferOverrunErr

Specifies the buffer overrun errors on the port.

### -field dwCompressionRatioIn

Specifies a percentage that indicates the degree to which data received on this connection is compressed. The ratio is the size of the compressed data divided by the size of the same data in an uncompressed state.

### -field dwCompressionRatioOut

Specifies a percentage indicating the degree to which data transmitted on this connection is compressed. The ratio is the size of the compressed data divided by the size of the same data in an uncompressed state.

## -see-also

<a href="/windows/desktop/RRAS/ras-administration-structures">RAS
		  Administration Structures</a>



<a href="/windows/desktop/api/mprapi/ne-mprapi-ras_hardware_condition">RAS_HARDWARE_CONDITION</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_port_0">RAS_PORT_0</a>



<a href="/windows/desktop/RRAS/remote-access-service-administration-reference">Remote Access Service Administration Reference</a>
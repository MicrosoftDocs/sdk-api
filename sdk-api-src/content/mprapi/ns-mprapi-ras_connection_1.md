---
UID: NS:mprapi._RAS_CONNECTION_1
title: RAS_CONNECTION_1 (mprapi.h)
description: The RAS_CONNECTION_1 structure contains detailed information regarding a specific connection, such as error counts and bytes received. For more general information about a specific connection, such as user name or domain, see RAS_CONNECTION_0.
helpviewer_keywords: ["*PRAS_CONNECTION_1","PRAS_CONNECTION_1","PRAS_CONNECTION_1 structure pointer [RAS]","RAS_CONNECTION_1","RAS_CONNECTION_1 structure [RAS]","_mpr_ras_connection_1","mprapi/PRAS_CONNECTION_1","mprapi/RAS_CONNECTION_1","rras.ras_connection_1"]
old-location: rras\ras_connection_1.htm
tech.root: RRAS
ms.assetid: 5f6c6895-4baf-46d7-865a-b95342b70abb
ms.date: 12/05/2018
ms.keywords: '*PRAS_CONNECTION_1, PRAS_CONNECTION_1, PRAS_CONNECTION_1 structure pointer [RAS], RAS_CONNECTION_1, RAS_CONNECTION_1 structure [RAS], _mpr_ras_connection_1, mprapi/PRAS_CONNECTION_1, mprapi/RAS_CONNECTION_1, rras.ras_connection_1'
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
req.typenames: RAS_CONNECTION_1, *PRAS_CONNECTION_1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RAS_CONNECTION_1
 - mprapi/_RAS_CONNECTION_1
 - PRAS_CONNECTION_1
 - mprapi/PRAS_CONNECTION_1
 - RAS_CONNECTION_1
 - mprapi/RAS_CONNECTION_1
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
 - RAS_CONNECTION_1
---

# RAS_CONNECTION_1 structure


## -description

The 
<b>RAS_CONNECTION_1</b> structure contains detailed information regarding a specific connection, such as error counts and bytes received. For more general information about a specific connection, such as user name or domain, see 
<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_0">RAS_CONNECTION_0</a>.

## -struct-fields

### -field hConnection

A handle to the connection.

### -field hInterface

A handle to the interface.

### -field PppInfo

A <a href="/windows/desktop/api/mprapi/ns-mprapi-ppp_info">PPP_INFO</a> structure that contains Point-to-Point (PPP) projection operation information for a connection.

### -field dwBytesXmited

A value that specifies the number of bytes transmitted on the connection.

### -field dwBytesRcved

A value that specifies the number of bytes received on the connection.

### -field dwFramesXmited

A value that specifies the number of frames transmitted on the connection.

### -field dwFramesRcved

A value that specifies the number of frames received on the connection.

### -field dwCrcErr

A value that specifies the number of Cyclic Redundancy Check (CRC) errors on the connection.

### -field dwTimeoutErr

A value that specifies the number of time-out errors on the connection.

### -field dwAlignmentErr

A value that specifies the number of alignment errors on the connection.

### -field dwHardwareOverrunErr

A value that specifies the number of hardware overrun errors on the connection.

### -field dwFramingErr

A value that specifies the number of framing errors on the connection.

### -field dwBufferOverrunErr

A value that specifies the number of buffer overrun errors on the connection.

### -field dwCompressionRatioIn

A value that specifies the percentage by which data received on this connection is compressed. <b>dwCompressionRatioIn</b> is the size of the compressed data divided by the size of the same data in an uncompressed state.

### -field dwCompressionRatioOut

A value that specifies the percentage by which data transmitted on this connection is compressed. The ratio is the size of the compressed data divided by the size of the same data in an uncompressed state.

## -see-also

<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminacceptreauthentication">MprAdminAcceptReauthentication</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionenum">MprAdminConnectionEnum</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionhangupnotification3">MprAdminConnectionHangupNotification3</a>



<a href="/windows/desktop/RRAS/ras-administration-structures">RAS Administration Structures</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_0">RAS_CONNECTION_0</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_2">RAS_CONNECTION_2</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_3">RAS_CONNECTION_3</a>



<a href="/windows/desktop/RRAS/remote-access-service-administration-reference">Remote Access Service Administration Reference</a>
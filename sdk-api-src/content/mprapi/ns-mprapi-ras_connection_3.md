---
UID: NS:mprapi._RAS_CONNECTION_3
title: RAS_CONNECTION_3 (mprapi.h)
description: The RAS_CONNECTION_3 structure contains information for the connection, including the Globally Unique Identifier (GUID) that identifies the connection and the quarantine state of the connection.
helpviewer_keywords: ["*PRAS_CONNECTION_3","PRAS_CONNECTION_3","PRAS_CONNECTION_3 structure pointer [RAS]","RAS_CONNECTION_3","RAS_CONNECTION_3 structure [RAS]","mprapi/PRAS_CONNECTION_3","mprapi/RAS_CONNECTION_3","rras.ras_connection_3"]
old-location: rras\ras_connection_3.htm
tech.root: RRAS
ms.assetid: f474563e-01c5-4f2a-aec4-477e0ffc7ab2
ms.date: 12/05/2018
ms.keywords: '*PRAS_CONNECTION_3, PRAS_CONNECTION_3, PRAS_CONNECTION_3 structure pointer [RAS], RAS_CONNECTION_3, RAS_CONNECTION_3 structure [RAS], mprapi/PRAS_CONNECTION_3, mprapi/RAS_CONNECTION_3, rras.ras_connection_3'
req.header: mprapi.h
req.include-header: 
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
targetos: Windows
req.typenames: RAS_CONNECTION_3, *PRAS_CONNECTION_3
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RAS_CONNECTION_3
 - mprapi/_RAS_CONNECTION_3
 - PRAS_CONNECTION_3
 - mprapi/PRAS_CONNECTION_3
 - RAS_CONNECTION_3
 - mprapi/RAS_CONNECTION_3
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
 - RAS_CONNECTION_3
---

# RAS_CONNECTION_3 structure


## -description

The 
<b>RAS_CONNECTION_3</b> structure contains information for the connection, including the Globally Unique Identifier (GUID) that identifies the connection and the quarantine state of the connection.

## -struct-fields

### -field dwVersion

The version of the <b>RAS_CONNECTION_3</b> structure used.

### -field dwSize

The size, in bytes, of this <b>RAS_CONNECTION_3</b> structure.

### -field hConnection

A handle to the connection.

### -field wszUserName

A null-terminated Unicode string that contains the name of the user logged on to the connection.

### -field dwInterfaceType

A <a href="/windows/desktop/api/mprapi/ne-mprapi-router_interface_type">ROUTER_INTERFACE_TYPE</a> enumeration that identifies the type of connection interface.

### -field guid

A GUID  that identifies the connection. For incoming connections, this GUID is valid only as long as the connection is active.

### -field PppInfo3

A 
<a href="/windows/desktop/api/mprapi/ns-mprapi-ppp_info_3">PPP_INFO_3</a> structure that contains Point-to-Point (PPP) projection operation information for a connection.

### -field rasQuarState

A <a href="/windows/desktop/api/mprapi/ne-mprapi-ras_quarantine_state">RAS_QUARANTINE_STATE</a> structure that specifies the Network Access Protection (NAP) quarantine state of the connection.

### -field timer

A FILETIME structure that specifies the time required for the connection to come out of quarantine after which the connection will be dropped. This value is valid only if <b>rasQuarState</b> has a value of <b>RAS_QUAR_STATE_PROBATION</b>.

## -see-also

<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminacceptreauthentication">MprAdminAcceptReauthentication</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionenum">MprAdminConnectionEnum</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionhangupnotification3">MprAdminConnectionHangupNotification3</a>



<a href="/windows/desktop/RRAS/ras-administration-structures">RAS Administration Structures</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_0">RAS_CONNECTION_0</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_1">RAS_CONNECTION_1</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_2">RAS_CONNECTION_2</a>



<a href="/windows/desktop/RRAS/remote-access-service-administration-reference">Remote Access Service Administration Reference</a>
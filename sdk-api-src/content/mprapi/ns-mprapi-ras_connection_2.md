---
UID: NS:mprapi._RAS_CONNECTION_2
title: RAS_CONNECTION_2 (mprapi.h)
description: The RAS_CONNECTION_2 structure contains information for a connection, including the Globally Unique Identifier (GUID) that identifies the connection.
helpviewer_keywords: ["*PRAS_CONNECTION_2","PRAS_CONNECTION_2","PRAS_CONNECTION_2 structure pointer [RAS]","RAS_CONNECTION_2","RAS_CONNECTION_2 structure [RAS]","_mpr_ras_connection_2","mprapi/PRAS_CONNECTION_2","mprapi/RAS_CONNECTION_2","rras.ras_connection_2"]
old-location: rras\ras_connection_2.htm
tech.root: RRAS
ms.assetid: 5dcc20f0-7447-4256-9dde-18a4a3c95816
ms.date: 12/05/2018
ms.keywords: '*PRAS_CONNECTION_2, PRAS_CONNECTION_2, PRAS_CONNECTION_2 structure pointer [RAS], RAS_CONNECTION_2, RAS_CONNECTION_2 structure [RAS], _mpr_ras_connection_2, mprapi/PRAS_CONNECTION_2, mprapi/RAS_CONNECTION_2, rras.ras_connection_2'
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
req.typenames: RAS_CONNECTION_2, *PRAS_CONNECTION_2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RAS_CONNECTION_2
 - mprapi/_RAS_CONNECTION_2
 - PRAS_CONNECTION_2
 - mprapi/PRAS_CONNECTION_2
 - RAS_CONNECTION_2
 - mprapi/RAS_CONNECTION_2
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
 - RAS_CONNECTION_2
---

# RAS_CONNECTION_2 structure


## -description

The 
<b>RAS_CONNECTION_2</b> structure contains information for a connection, including the Globally Unique Identifier (GUID) that identifies the connection.

## -struct-fields

### -field hConnection

A handle to the connection.

### -field wszUserName

A null-terminated Unicode string that contains the name of the user logged on to the connection.

### -field dwInterfaceType

A <a href="/windows/desktop/api/mprapi/ne-mprapi-router_interface_type">ROUTER_INTERFACE_TYPE</a> enumeration that identifies the type of connection interface.

### -field guid

A GUID  that identifies the connection. For incoming connections, this GUID is valid only as long as the connection is active.

### -field PppInfo2

A 
<a href="/windows/desktop/api/mprapi/ns-mprapi-ppp_info_2">PPP_INFO_2</a> structure that contains Point-to-Point (PPP) projection operation information for a connection.

## -see-also

<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminacceptreauthentication">MprAdminAcceptReauthentication</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionenum">MprAdminConnectionEnum</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionhangupnotification3">MprAdminConnectionHangupNotification3</a>



<a href="/windows/desktop/RRAS/ras-administration-structures">RAS Administration Structures</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_0">RAS_CONNECTION_0</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_1">RAS_CONNECTION_1</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_3">RAS_CONNECTION_3</a>



<a href="/windows/desktop/RRAS/remote-access-service-administration-reference">Remote Access Service Administration Reference</a>
---
UID: NS:tssbx.__MIDL_IWTSSBPlugin_0009
title: WTSSBX_SESSION_INFO (tssbx.h)
description: Contains information about sessions that are available to Remote Desktop Connection Broker (RD Connection Broker).
helpviewer_keywords: ["WTSSBX_SESSION_INFO","WTSSBX_SESSION_INFO structure [Remote Desktop Services]","__MIDL_IWTSSBPlugin_0009","termserv.wtssbx_session_info","tssbx/WTSSBX_SESSION_INFO"]
old-location: termserv\wtssbx_session_info.htm
tech.root: TermServ
ms.assetid: d0c142a9-2495-46e6-b53b-0c415bddb0b2
ms.date: 12/05/2018
ms.keywords: WTSSBX_SESSION_INFO, WTSSBX_SESSION_INFO structure [Remote Desktop Services], __MIDL_IWTSSBPlugin_0009, termserv.wtssbx_session_info, tssbx/WTSSBX_SESSION_INFO
req.header: tssbx.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tssbx.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WTSSBX_SESSION_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL_IWTSSBPlugin_0009
 - tssbx/__MIDL_IWTSSBPlugin_0009
 - WTSSBX_SESSION_INFO
 - tssbx/WTSSBX_SESSION_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tssbx.h
api_name:
 - WTSSBX_SESSION_INFO
---

# WTSSBX_SESSION_INFO structure


## -description

Contains information about sessions that are available to Remote Desktop Connection Broker (RD Connection Broker).

## -struct-fields

### -field wszUserName

The user name that is associated with the session. The name cannot exceed 104 characters.

### -field wszDomainName

The domain name of the user. The name cannot exceed 256 characters.

### -field ApplicationType

The name of the program that should be run after the session is created. The name cannot exceed 256 characters.

### -field dwSessionId

The session identifier.

### -field CreateTime

The time that the session was initiated.

### -field DisconnectTime

The time that the user disconnected from the session.

### -field SessionState

A value of the <a href="/windows/win32/api/tssbx/ne-tssbx-wtssbx_session_state">WTSSBX_SESSION_STATE</a> enumeration type that indicates the state of the session.

## -see-also

<a href="/windows/desktop/api/tssbx/nn-tssbx-iwtssbplugin">IWTSSBPlugin</a>
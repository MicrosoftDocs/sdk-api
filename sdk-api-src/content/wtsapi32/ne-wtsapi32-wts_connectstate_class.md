---
UID: NE:wtsapi32._WTS_CONNECTSTATE_CLASS
title: WTS_CONNECTSTATE_CLASS (wtsapi32.h)
description: Specifies the connection state of a Remote Desktop Services session.
helpviewer_keywords: ["WTSActive","WTSConnectQuery","WTSConnected","WTSDisconnected","WTSDown","WTSIdle","WTSInit","WTSListen","WTSReset","WTSShadow","WTS_CONNECTSTATE_CLASS","WTS_CONNECTSTATE_CLASS enumeration [Remote Desktop Services]","_win32_wts_connectstate_class_str","termserv.wts_connectstate_class_str","wtsapi32/WTSActive","wtsapi32/WTSConnectQuery","wtsapi32/WTSConnected","wtsapi32/WTSDisconnected","wtsapi32/WTSDown","wtsapi32/WTSIdle","wtsapi32/WTSInit","wtsapi32/WTSListen","wtsapi32/WTSReset","wtsapi32/WTSShadow","wtsapi32/WTS_CONNECTSTATE_CLASS"]
old-location: termserv\wts_connectstate_class_str.htm
tech.root: TermServ
ms.assetid: ee376f5a-3474-4e31-94c1-e760346eb794
ms.date: 12/05/2018
ms.keywords: WTSActive, WTSConnectQuery, WTSConnected, WTSDisconnected, WTSDown, WTSIdle, WTSInit, WTSListen, WTSReset, WTSShadow, WTS_CONNECTSTATE_CLASS, WTS_CONNECTSTATE_CLASS enumeration [Remote Desktop Services], _win32_wts_connectstate_class_str, termserv.wts_connectstate_class_str, wtsapi32/WTSActive, wtsapi32/WTSConnectQuery, wtsapi32/WTSConnected, wtsapi32/WTSDisconnected, wtsapi32/WTSDown, wtsapi32/WTSIdle, wtsapi32/WTSInit, wtsapi32/WTSListen, wtsapi32/WTSReset, wtsapi32/WTSShadow, wtsapi32/WTS_CONNECTSTATE_CLASS
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: WTS_CONNECTSTATE_CLASS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WTS_CONNECTSTATE_CLASS
 - wtsapi32/_WTS_CONNECTSTATE_CLASS
 - WTS_CONNECTSTATE_CLASS
 - wtsapi32/WTS_CONNECTSTATE_CLASS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wtsapi32.h
api_name:
 - WTS_CONNECTSTATE_CLASS
---

# WTS_CONNECTSTATE_CLASS enumeration


## -description

Specifies the connection state of a Remote Desktop Services session.

## -enum-fields

### -field WTSActive

A user is logged on to the WinStation. This state occurs when a user is signed in and actively connected to the device.

### -field WTSConnected

The WinStation is connected to the client.

### -field WTSConnectQuery

The WinStation is in the process of connecting to the client.

### -field WTSShadow

The WinStation is shadowing another WinStation.

### -field WTSDisconnected

The WinStation is active but the client is disconnected. This state occurs when a user is signed in but not actively connected to the device, such as when the user has chosen to exit to the lock screen.

### -field WTSIdle

The WinStation is waiting for a client to connect.

### -field WTSListen

The WinStation is listening for a connection. A listener session waits for requests for new client connections. No user is logged on a listener session. A listener session cannot be reset, shadowed, or changed to a regular client session.

### -field WTSReset

The WinStation is being reset.

### -field WTSDown

The WinStation is down due to an error.

### -field WTSInit

The WinStation is initializing.

## -see-also

<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsquerysessioninformationa">WTSQuerySessionInformation</a>



<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtswaitsystemevent">WTSWaitSystemEvent</a>



<a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wts_session_infoa">WTS_SESSION_INFO</a>

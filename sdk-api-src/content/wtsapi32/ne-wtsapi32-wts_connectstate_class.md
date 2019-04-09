---
UID: NE:wtsapi32._WTS_CONNECTSTATE_CLASS
title: WTS_CONNECTSTATE_CLASS (wtsapi32.h)
author: windows-sdk-content
description: Specifies the connection state of a Remote Desktop Services session.
old-location: termserv\wts_connectstate_class_str.htm
tech.root: TermServ
ms.assetid: ee376f5a-3474-4e31-94c1-e760346eb794
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WTSActive, WTSConnectQuery, WTSConnected, WTSDisconnected, WTSDown, WTSIdle, WTSInit, WTSListen, WTSReset, WTSShadow, WTS_CONNECTSTATE_CLASS, WTS_CONNECTSTATE_CLASS enumeration [Remote Desktop Services], _win32_wts_connectstate_class_str, termserv.wts_connectstate_class_str, wtsapi32/WTSActive, wtsapi32/WTSConnectQuery, wtsapi32/WTSConnected, wtsapi32/WTSDisconnected, wtsapi32/WTSDown, wtsapi32/WTSIdle, wtsapi32/WTSInit, wtsapi32/WTSListen, wtsapi32/WTSReset, wtsapi32/WTSShadow, wtsapi32/WTS_CONNECTSTATE_CLASS
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wtsapi32.h
api_name:
 - WTS_CONNECTSTATE_CLASS
product: Windows
targetos: Windows
req.typenames: WTS_CONNECTSTATE_CLASS
req.redist: 
---

# WTS_CONNECTSTATE_CLASS enumeration


## -description


Specifies the connection state of a Remote Desktop Services session.


## -enum-fields




### -field WTSActive

A user is logged on to the WinStation.


### -field WTSConnected

The WinStation is connected to the client.


### -field WTSConnectQuery

The WinStation is in the process of connecting to the client.


### -field WTSShadow

The WinStation is shadowing another WinStation.


### -field WTSDisconnected

The WinStation is active but the client is disconnected.


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




<a href="https://msdn.microsoft.com/d52345a4-0408-4ea9-ba71-349910143752">WTSQuerySessionInformation</a>



<a href="https://msdn.microsoft.com/4139c009-6d2f-460b-b7a0-097bd2218505">WTSWaitSystemEvent</a>



<a href="https://msdn.microsoft.com/bb40d928-293a-4e2c-b7cf-2ac038da53c2">WTS_SESSION_INFO</a>
 

 


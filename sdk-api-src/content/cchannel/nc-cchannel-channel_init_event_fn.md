---
UID: NC:cchannel.CHANNEL_INIT_EVENT_FN
title: CHANNEL_INIT_EVENT_FN (cchannel.h)
description: An application-defined callback function that Remote Desktop Services calls to notify the client DLL of virtual channel events.
helpviewer_keywords: ["CHANNEL_EVENT_CONNECTED","CHANNEL_EVENT_DISCONNECTED","CHANNEL_EVENT_INITIALIZED","CHANNEL_EVENT_REMOTE_CONTROL_START","CHANNEL_EVENT_REMOTE_CONTROL_STOP","CHANNEL_EVENT_TERMINATED","CHANNEL_EVENT_V1_CONNECTED","CHANNEL_INIT_EVENT_FN","CHANNEL_INIT_EVENT_FN callback function [Remote Desktop Services]","VirtualChannelInitEvent callback","_win32_virtualchannelinitevent","cchannel/CHANNEL_INIT_EVENT_FN","termserv.virtualchannelinitevent"]
old-location: termserv\virtualchannelinitevent.htm
tech.root: TermServ
ms.assetid: 8a074b6c-7fc1-411f-a50c-64f40c0c4dd6
ms.date: 12/05/2018
ms.keywords: CHANNEL_EVENT_CONNECTED, CHANNEL_EVENT_DISCONNECTED, CHANNEL_EVENT_INITIALIZED, CHANNEL_EVENT_REMOTE_CONTROL_START, CHANNEL_EVENT_REMOTE_CONTROL_STOP, CHANNEL_EVENT_TERMINATED, CHANNEL_EVENT_V1_CONNECTED, CHANNEL_INIT_EVENT_FN, CHANNEL_INIT_EVENT_FN callback function [Remote Desktop Services], VirtualChannelInitEvent callback, _win32_virtualchannelinitevent, cchannel/CHANNEL_INIT_EVENT_FN, termserv.virtualchannelinitevent
req.header: cchannel.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CHANNEL_INIT_EVENT_FN
 - cchannel/CHANNEL_INIT_EVENT_FN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Cchannel.h
api_name:
 - CHANNEL_INIT_EVENT_FN
---

# CHANNEL_INIT_EVENT_FN callback function


## -description

An application-defined callback 
    function that Remote Desktop Services calls to notify the client DLL of virtual channel events.

The <b>PCHANNEL_INIT_EVENT_FN</b> type defines a pointer to this callback function. 
    <b>VirtualChannelInitEvent</b> is a placeholder for the application-defined or 
    library-defined function name.

## -parameters

### -param pInitHandle [in]

Handle to the client connection. This is the handle returned in the <i>ppInitHandle</i> parameter of the 
      <a href="/windows/desktop/api/cchannel/nc-cchannel-virtualchannelinit">VirtualChannelInit</a> function.

### -param event [in]

Indicates the event that caused the notification. This parameter can be one of the following values.



#### CHANNEL_EVENT_INITIALIZED (0)

The Remote Desktop Connection (RDC) client initialization has been completed. The <i>pData</i> parameter is <b>NULL</b>.



#### CHANNEL_EVENT_CONNECTED (1)

A connection has been established with an RD Session Host server that supports virtual channels. The 
         <i>pData</i> parameter is a pointer to a <b>null</b>-terminated string with the name of the server.



#### CHANNEL_EVENT_V1_CONNECTED (2)

A connection has been established with an RD Session Host server that does not support virtual channels. The 
         <i>pData</i> parameter is <b>NULL</b>.



#### CHANNEL_EVENT_DISCONNECTED (3)

The connection to the RD Session Host server has been disconnected. The <i>pData</i> parameter is <b>NULL</b>.



#### CHANNEL_EVENT_TERMINATED (4)

The client has been terminated. The <i>pData</i> parameter is <b>NULL</b>.



#### CHANNEL_EVENT_REMOTE_CONTROL_START (5)

A remote control operation has been started. The <i>pData</i> parameter is <b>NULL</b>.



#### CHANNEL_EVENT_REMOTE_CONTROL_STOP (6)

A remote control operation has been terminated. The <i>pData</i> parameter is a pointer to a 
         <b>null</b>-terminated string containing the name of the server.

### -param pData [in]

Pointer to additional data for the event. The type of data depends on the event, as described previously 
       in the event descriptions.

### -param dataLength [in]

Specifies the size, in bytes, of the data in the <i>pData</i> buffer.

## -returns

This function does not return a value.

## -remarks

The client DLL uses the 
     <a href="/windows/desktop/api/cchannel/nc-cchannel-virtualchannelinit">VirtualChannelInit</a> function to 
     register its <b>VirtualChannelInitEvent</b> function with Remote Desktop Services.

This function is reentrant on a per-handle basis. The function may be called while it is executing, but not 
     on the same handle more than once.

This function is called only after 
     <a href="/windows/desktop/api/cchannel/nc-cchannel-virtualchannelentry">VirtualChannelEntry</a> has completed.

<b>CHANNEL_EVENT_CONNECTED</b> and <b>CHANNEL_EVENT_DISCONNECTED</b> event notifications will not be sent if the 
     connection is transferred to another session. However, the server-side plug-in that is administering the session 
     to which the connection is transferred will receive a reconnection notification. A server-side tool such as 
     Tscon.exe can be used to transfer connections. Refer to 
     <a href="/windows/desktop/TermServ/monitoring-session-connections-and-disconnections">Monitoring Session 
     Connections and Disconnections</a> for more information on reconnection notifications.

If the user-mode plug-in must be notified that it has been reconnected (for example, if it must reset its 
     state),  the server-side plug-in should send a notification message to the client. This notification should 
     use the protocol that the plug-ins use to communicate with each other.

## -see-also

<a href="/windows/desktop/api/cchannel/nc-cchannel-virtualchannelinit">VirtualChannelInit</a>
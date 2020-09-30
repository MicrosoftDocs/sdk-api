---
UID: NF:wtsapi32.WTSWaitSystemEvent
title: WTSWaitSystemEvent function (wtsapi32.h)
description: Waits for a Remote Desktop Services event before returning to the caller.
helpviewer_keywords: ["WTSWaitSystemEvent","WTSWaitSystemEvent function [Remote Desktop Services]","WTS_EVENT_ALL","WTS_EVENT_CONNECT","WTS_EVENT_CREATE","WTS_EVENT_DELETE","WTS_EVENT_DISCONNECT","WTS_EVENT_LICENSE","WTS_EVENT_LOGOFF","WTS_EVENT_LOGON","WTS_EVENT_RENAME","WTS_EVENT_STATECHANGE","_win32_wtswaitsystemevent","termserv.wtswaitsystemevent","wtsapi32/WTSWaitSystemEvent"]
old-location: termserv\wtswaitsystemevent.htm
tech.root: TermServ
ms.assetid: 4139c009-6d2f-460b-b7a0-097bd2218505
ms.date: 12/05/2018
ms.keywords: WTSWaitSystemEvent, WTSWaitSystemEvent function [Remote Desktop Services], WTS_EVENT_ALL, WTS_EVENT_CONNECT, WTS_EVENT_CREATE, WTS_EVENT_DELETE, WTS_EVENT_DISCONNECT, WTS_EVENT_LICENSE, WTS_EVENT_LOGOFF, WTS_EVENT_LOGON, WTS_EVENT_RENAME, WTS_EVENT_STATECHANGE, _win32_wtswaitsystemevent, termserv.wtswaitsystemevent, wtsapi32/WTSWaitSystemEvent
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
req.lib: Wtsapi32.lib
req.dll: Wtsapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WTSWaitSystemEvent
 - wtsapi32/WTSWaitSystemEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wtsapi32.dll
api_name:
 - WTSWaitSystemEvent
---

# WTSWaitSystemEvent function


## -description

Waits for a Remote Desktop Services event before returning to the caller.

## -parameters

### -param hServer [in]

Handle to an RD Session Host server. Specify a handle opened by the 
<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsopenservera">WTSOpenServer</a> function, or specify WTS_CURRENT_SERVER_HANDLE to indicate the RD Session Host server on which your application is running.

### -param EventMask [in]

Bitmask that specifies the set of events to wait for. This mask can be WTS_EVENT_FLUSH to cause all pending 
<b>WTSWaitSystemEvent</b> calls on the specified RD Session Host server handle to return. Or, the mask can be a combination of the following values.



#### WTS_EVENT_ALL

Wait for any event type.



#### WTS_EVENT_CONNECT

A client connected to a WinStation.



#### WTS_EVENT_CREATE

A new WinStation was created.



#### WTS_EVENT_DELETE

An existing WinStation was deleted.



#### WTS_EVENT_DISCONNECT

A client disconnected from a WinStation.



#### WTS_EVENT_LICENSE

The Remote Desktop Services' license state changed. This occurs when a license is added or deleted using 
        License Manager.



#### WTS_EVENT_LOGOFF

A user logged off from either the Remote Desktop Services console or from a client WinStation.



#### WTS_EVENT_LOGON

A user logged on to the system from either the Remote Desktop Services console or from a client WinStation.



#### WTS_EVENT_RENAME

An existing WinStation was renamed.



#### WTS_EVENT_STATECHANGE

A WinStation connection state changed. For a list of connection states, see the 
        <a href="/windows/desktop/api/wtsapi32/ne-wtsapi32-wts_connectstate_class">WTS_CONNECTSTATE_CLASS</a> enumeration 
        type.

### -param pEventFlags [out]

Pointer to a variable that receives a bitmask of the event or events that occurred. The returned mask can 
      be a combination of the values from the previous list, or it can be <b>WTS_EVENT_NONE</b> if 
      the wait terminated because of a <b>WTSWaitSystemEvent</b> call with 
      <b>WTS_EVENT_FLUSH</b>.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsopenservera">WTSOpenServer</a>
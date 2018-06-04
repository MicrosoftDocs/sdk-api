---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# WTSWaitSystemEvent function


## -description


Waits for a Remote Desktop Services event before returning to the caller.


## -parameters




### -param hServer [in]

Handle to an RD Session Host server. Specify a handle opened by the 
<a href="https://msdn.microsoft.com/f0b7dce7-59eb-41b8-9a61-65a69d1cc1f3">WTSOpenServer</a> function, or specify WTS_CURRENT_SERVER_HANDLE to indicate the RD Session Host server on which your application is running.


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
        <a href="https://msdn.microsoft.com/ee376f5a-3474-4e31-94c1-e760346eb794">WTS_CONNECTSTATE_CLASS</a> enumeration 
        type.


### -param pEventFlags [out]

Pointer to a variable that receives a bitmask of the event or events that occurred. The returned mask can 
      be a combination of the values from the previous list, or it can be <b>WTS_EVENT_NONE</b> if 
      the wait terminated because of a <b>WTSWaitSystemEvent</b> call with 
      <b>WTS_EVENT_FLUSH</b>.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/f0b7dce7-59eb-41b8-9a61-65a69d1cc1f3">WTSOpenServer</a>
 

 


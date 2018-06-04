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

# IWTSProtocolManager::NotifySessionStateChange


## -description


<p class="CCE_Message">[<b>IWTSProtocolManager::NotifySessionStateChange</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/72438718-1a66-473b-a563-67cfc8095318">IWRdsProtocolManager::NotifySessionStateChange</a>.]

Notifies the protocol provider of changes in the state of a session.


## -parameters




### -param SessionId [in]

A pointer to a <a href="https://msdn.microsoft.com/fe0714ec-c670-40b7-9808-2171abae79a8">WTS_SESSION_ID</a> structure that uniquely identifies the session.


### -param EventId [in]

An integer that contains the event ID. The following IDs can be found in Winuser.h.



#### WTS_CONSOLE_CONNECT (0x1)



#### WTS_CONSOLE_DISCONNECT (0x2)



#### WTS_REMOTE_CONNECT (0x3)



#### WTS_SESSION_LOGOFF (0x6)



#### WTS_SESSION_LOCK (0x7)



#### WTS_SESSION_UNLOCK (0x8)



#### WTS_SESSION_REMOTE_CONTROL (0x9)


## -returns



When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/a54bdb46-b18b-4a6d-90fc-75947f6dd191">IWTSProtocolManager</a>
 

 


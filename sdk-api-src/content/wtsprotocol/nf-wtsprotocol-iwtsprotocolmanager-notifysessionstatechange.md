---
UID: NF:wtsprotocol.IWTSProtocolManager.NotifySessionStateChange
title: IWTSProtocolManager::NotifySessionStateChange
author: windows-sdk-content
description: IWTSProtocolManager::NotifySessionStateChange is no longer available. Instead, use IWRdsProtocolManager::NotifySessionStateChange.
old-location: termserv\iwtsprotocolmanager_notifysessionstatechange.htm
old-project: TermServ
ms.assetid: 59c284bf-8175-46d2-ab44-8b2975574c14
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IWTSProtocolManager interface [Remote Desktop Services],NotifySessionStateChange method, IWTSProtocolManager.NotifySessionStateChange, IWTSProtocolManager::NotifySessionStateChange, NotifySessionStateChange, NotifySessionStateChange method [Remote Desktop Services], NotifySessionStateChange method [Remote Desktop Services],IWTSProtocolManager interface, WTS_CONSOLE_CONNECT, WTS_CONSOLE_DISCONNECT, WTS_REMOTE_CONNECT, WTS_SESSION_LOCK, WTS_SESSION_LOGOFF, WTS_SESSION_REMOTE_CONTROL, WTS_SESSION_UNLOCK, termserv.iwtsprotocolmanager_notifysessionstatechange, wtsprotocol/IWTSProtocolManager::NotifySessionStateChange
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wtsprotocol.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wtsprotocol.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WTS_PROPERTY_VALUE, *PWTS_PROPERTY_VALUE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wtsprotocol.h
api_name:
-	IWTSProtocolManager.NotifySessionStateChange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
 

 


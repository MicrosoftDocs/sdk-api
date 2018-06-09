---
UID: NF:wtsprotocol.IWTSProtocolConnection.NotifySessionId
title: IWTSProtocolConnection::NotifySessionId
author: windows-sdk-content
description: IWTSProtocolConnection::NotifySessionId is no longer available. Instead, use IWRdsProtocolConnection::NotifySessionId.
old-location: termserv\iwtsprotocolconnection_notifysessionid.htm
old-project: TermServ
ms.assetid: 5a545f66-7143-419d-9e0c-a96070472ce5
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IWTSProtocolConnection interface [Remote Desktop Services],NotifySessionId method, IWTSProtocolConnection.NotifySessionId, IWTSProtocolConnection::NotifySessionId, NotifySessionId, NotifySessionId method [Remote Desktop Services], NotifySessionId method [Remote Desktop Services],IWTSProtocolConnection interface, termserv.iwtsprotocolconnection_notifysessionid, wtsprotocol/IWTSProtocolConnection::NotifySessionId
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
tech.root: 
req.typenames: WTS_PROPERTY_VALUE, *PWTS_PROPERTY_VALUE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wtsprotocol.h
api_name:
 - IWTSProtocolConnection.NotifySessionId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWTSProtocolConnection::NotifySessionId


## -description


<p class="CCE_Message">[<b>IWTSProtocolConnection::NotifySessionId</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/82bf892e-5e6f-4057-ac36-00e046080c93">IWRdsProtocolConnection::NotifySessionId</a>.]

Sends the ID of  the new session to the protocol.


## -parameters




### -param SessionId [in]

A pointer to a <a href="https://msdn.microsoft.com/fe0714ec-c670-40b7-9808-2171abae79a8">WTS_SESSION_ID</a> structure that contains a connection GUID and the associated session ID.


## -remarks



This is an event notification and you should return immediately from this method. To avoid a possible deadlock, you should not make any function or method calls that will directly or indirectly result in a Remote Desktop Services API being called. If you need to make any outbound call, you should start a new thread and make the outbound call from the new thread.




## -see-also




<a href="https://msdn.microsoft.com/584a6874-0df4-480e-a10a-4b603643870e">IWTSProtocolConnection</a>
 

 


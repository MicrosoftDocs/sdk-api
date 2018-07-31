---
UID: NF:wtsprotocol.IWTSProtocolConnection.LogonNotify
title: IWTSProtocolConnection::LogonNotify
author: windows-sdk-content
description: IWTSProtocolConnection::LogonNotify is no longer available. Instead, use IWRdsProtocolConnection::LogonNotify.
old-location: termserv\iwtsprotocolconnection_logonnotify.htm
old-project: TermServ
ms.assetid: 6065e827-23a5-4150-bda5-999b7acede65
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IWTSProtocolConnection interface [Remote Desktop Services],LogonNotify method, IWTSProtocolConnection.LogonNotify, IWTSProtocolConnection::LogonNotify, LogonNotify, LogonNotify method [Remote Desktop Services], LogonNotify method [Remote Desktop Services],IWTSProtocolConnection interface, termserv.iwtsprotocolconnection_logonnotify, wtsprotocol/IWTSProtocolConnection::LogonNotify
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
 - IWTSProtocolConnection.LogonNotify
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWTSProtocolConnection::LogonNotify


## -description


<p class="CCE_Message">[<b>IWTSProtocolConnection::LogonNotify</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/2b6ce1cd-0e9f-465d-a5d6-e0d35bddebc4">IWRdsProtocolConnection::LogonNotify</a>.]

Specifies that the user has logged on to the session.


## -parameters




### -param hClientToken [in]

A pointer to a user token handle.


### -param wszUserName [in]

A pointer to a string that contains the user name.


### -param wszDomainName [in]

A pointer to a string that contains the domain name for the user.


### -param SessionId [in]

A pointer to a <a href="https://msdn.microsoft.com/fe0714ec-c670-40b7-9808-2171abae79a8">WTS_SESSION_ID</a> structure that contains the session ID associated with the user.


## -remarks



The Remote Desktop Services service also calls this method when  the state of the session has changed.

This is an event notification and you should return immediately from this method. To avoid a possible deadlock, you should not make any function or method calls that will directly or indirectly result in a <a href="https://msdn.microsoft.com/e99a86ee-af0e-46db-8dad-69703ca84fa0">Remote Desktop Services API</a> being called. If you need to make any outbound call, you should start a new thread and make the outbound call from the new thread.




## -see-also




<a href="https://msdn.microsoft.com/584a6874-0df4-480e-a10a-4b603643870e">IWTSProtocolConnection</a>
 

 


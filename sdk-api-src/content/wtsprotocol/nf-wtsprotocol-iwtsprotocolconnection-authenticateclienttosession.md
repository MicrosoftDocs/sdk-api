---
UID: NF:wtsprotocol.IWTSProtocolConnection.AuthenticateClientToSession
title: IWTSProtocolConnection::AuthenticateClientToSession
author: windows-sdk-content
description: IWTSProtocolConnection::AuthenticateClientToSession is no longer available. Instead, use IWRdsProtocolConnection::AuthenticateClientToSession.
old-location: termserv\iwtsprotocolconnection_authenticateclienttosession.htm
old-project: TermServ
ms.assetid: 541bf463-9a4a-4237-8a61-1288ab1540cc
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: AuthenticateClientToSession, AuthenticateClientToSession method [Remote Desktop Services], AuthenticateClientToSession method [Remote Desktop Services],IWTSProtocolConnection interface, IWTSProtocolConnection interface [Remote Desktop Services],AuthenticateClientToSession method, IWTSProtocolConnection.AuthenticateClientToSession, IWTSProtocolConnection::AuthenticateClientToSession, termserv.iwtsprotocolconnection_authenticateclienttosession, wtsprotocol/IWTSProtocolConnection::AuthenticateClientToSession
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
-	IWTSProtocolConnection.AuthenticateClientToSession
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWTSProtocolConnection::AuthenticateClientToSession


## -description


<p class="CCE_Message">[<b>IWTSProtocolConnection::AuthenticateClientToSession</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/314f1ae8-5b2d-4c95-bb2d-0d9288d38934">IWRdsProtocolConnection::AuthenticateClientToSession</a>.]

Specifies a session that the connection should be reconnected to.


## -parameters




### -param SessionId [out]

A pointer to a <a href="https://msdn.microsoft.com/fe0714ec-c670-40b7-9808-2171abae79a8">WTS_SESSION_ID</a> structure that uniquely identifies the session.


## -see-also




<a href="https://msdn.microsoft.com/584a6874-0df4-480e-a10a-4b603643870e">IWTSProtocolConnection</a>
 

 


---
UID: NF:wtsprotocol.IWTSProtocolConnection.SessionArbitrationEnumeration
title: IWTSProtocolConnection::SessionArbitrationEnumeration
author: windows-sdk-content
description: IWTSProtocolConnection::SessionArbitrationEnumeration is no longer available. Instead, use IWRdsProtocolConnection::SessionArbitrationEnumeration.
old-location: termserv\iwtsprotocolconnection_sessionarbitrationenumeration.htm
old-project: TermServ
ms.assetid: 413d6df5-419f-4a68-bb91-dfec9f455b42
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IWTSProtocolConnection interface [Remote Desktop Services],SessionArbitrationEnumeration method, IWTSProtocolConnection.SessionArbitrationEnumeration, IWTSProtocolConnection::SessionArbitrationEnumeration, SessionArbitrationEnumeration, SessionArbitrationEnumeration method [Remote Desktop Services], SessionArbitrationEnumeration method [Remote Desktop Services],IWTSProtocolConnection interface, termserv.iwtsprotocolconnection_sessionarbitrationenumeration, wtsprotocol/IWTSProtocolConnection::SessionArbitrationEnumeration
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
 - IWTSProtocolConnection.SessionArbitrationEnumeration
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWTSProtocolConnection::SessionArbitrationEnumeration


## -description


<p class="CCE_Message">[<b>IWTSProtocolConnection::SessionArbitrationEnumeration</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/d0e93014-1f79-47ac-bf3a-c100eb652751">IWRdsProtocolConnection::SessionArbitrationEnumeration</a>.]

Retrieves a collection of session IDs for reconnection.


## -parameters




### -param hUserToken [in]

A pointer to a user token handle.


### -param bSingleSessionPerUserEnabled [in]

A Boolean value that specifies whether a user can be associated with, at most, one session.


### -param pSessionIdArray [out]

A pointer to an array of integers that contains the disconnected session IDs for the user.


### -param pdwSessionIdentifierCount [in, out]

A pointer to an integer that specifies the number of disconnected session IDs referenced by  the <i>pSessionIdArray</i> parameter.


## -remarks



The Remote Desktop Services service calls this method to find existing sessions that this user can reconnect to. If this method returns an <b>HRESULT</b> error code or it does not return any session IDs,  the Remote Desktop Services service performs arbitration itself.




## -see-also




<a href="https://msdn.microsoft.com/584a6874-0df4-480e-a10a-4b603643870e">IWTSProtocolConnection</a>
 

 


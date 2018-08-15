---
UID: NF:wtsprotocol.IWRdsProtocolConnection.AuthenticateClientToSession
title: IWRdsProtocolConnection::AuthenticateClientToSession
author: windows-sdk-content
description: Specifies a session that the connection should be reconnected to.
old-location: termserv\iwrdsprotocolconnection_authenticateclienttosession.htm
old-project: termserv
ms.assetid: 314f1ae8-5b2d-4c95-bb2d-0d9288d38934
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: AuthenticateClientToSession, AuthenticateClientToSession method [Remote Desktop Services], AuthenticateClientToSession method [Remote Desktop Services],IWRdsProtocolConnection interface, IWRdsProtocolConnection interface [Remote Desktop Services],AuthenticateClientToSession method, IWRdsProtocolConnection.AuthenticateClientToSession, IWRdsProtocolConnection::AuthenticateClientToSession, termserv.iwrdsprotocolconnection_authenticateclienttosession, wtsprotocol/IWRdsProtocolConnection::AuthenticateClientToSession
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wtsprotocol.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
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
 - wtsprotocol.h
api_name:
 - IWRdsProtocolConnection.AuthenticateClientToSession
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWRdsProtocolConnection::AuthenticateClientToSession


## -description


Specifies a session that the connection should be reconnected to.


## -parameters




### -param SessionId [out]

A pointer to a <a href="https://msdn.microsoft.com/fe0714ec-c670-40b7-9808-2171abae79a8">WRDS_SESSION_ID</a> structure that uniquely identifies the session.


## -returns



If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

Upon receiving an error, the Remote Desktop Services service continues the connection sequence.




## -see-also




<a href="https://msdn.microsoft.com/2b8a5b2f-5a54-4d60-8b5a-8a914728087c">IWRdsProtocolConnection</a>
 

 


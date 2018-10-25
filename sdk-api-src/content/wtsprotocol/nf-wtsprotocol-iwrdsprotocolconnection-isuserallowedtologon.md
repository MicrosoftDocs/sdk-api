---
UID: NF:wtsprotocol.IWRdsProtocolConnection.IsUserAllowedToLogon
title: IWRdsProtocolConnection::IsUserAllowedToLogon
author: windows-sdk-content
description: Determines from the protocol whether a user is allowed to log on to a session.
old-location: termserv\iwrdsprotocolconnection_isuserallowedtologon.htm
tech.root: termserv
ms.assetid: 4e2c5d2b-ec45-45ea-8bd3-71aaa0b15529
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: IWRdsProtocolConnection interface [Remote Desktop Services],IsUserAllowedToLogon method, IWRdsProtocolConnection.IsUserAllowedToLogon, IWRdsProtocolConnection::IsUserAllowedToLogon, IsUserAllowedToLogon, IsUserAllowedToLogon method [Remote Desktop Services], IsUserAllowedToLogon method [Remote Desktop Services],IWRdsProtocolConnection interface, termserv.iwrdsprotocolconnection_isuserallowedtologon, wtsprotocol/IWRdsProtocolConnection::IsUserAllowedToLogon
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wtsprotocol.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wtsprotocol.h
api_name:
 - IWRdsProtocolConnection.IsUserAllowedToLogon
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWRdsProtocolConnection::IsUserAllowedToLogon


## -description


Determines from the protocol whether a user is allowed to log on to a session.


## -parameters




### -param SessionId [in]

The session identifier.


### -param UserToken [in]

A handle that represents the user token.


### -param pDomainName [in]

A pointer to a null-terminated string that contains the user's domain name.


### -param pUserName [in]

A pointer to a null-terminated string that contains the user name.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/2b8a5b2f-5a54-4d60-8b5a-8a914728087c">IWRdsProtocolConnection</a>
 

 


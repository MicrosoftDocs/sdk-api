---
UID: NF:wtsprotocol.IWRdsProtocolConnection.IsUserAllowedToLogon
title: IWRdsProtocolConnection::IsUserAllowedToLogon (wtsprotocol.h)
description: Determines from the protocol whether a user is allowed to log on to a session.
old-location: termserv\iwrdsprotocolconnection_isuserallowedtologon.htm
tech.root: TermServ
ms.assetid: 4e2c5d2b-ec45-45ea-8bd3-71aaa0b15529
ms.date: 12/05/2018
ms.keywords: IWRdsProtocolConnection interface [Remote Desktop Services],IsUserAllowedToLogon method, IWRdsProtocolConnection.IsUserAllowedToLogon, IWRdsProtocolConnection::IsUserAllowedToLogon, IsUserAllowedToLogon, IsUserAllowedToLogon method [Remote Desktop Services], IsUserAllowedToLogon method [Remote Desktop Services],IWRdsProtocolConnection interface, termserv.iwrdsprotocolconnection_isuserallowedtologon, wtsprotocol/IWRdsProtocolConnection::IsUserAllowedToLogon
ms.topic: method
f1_keywords:
- wtsprotocol/IWRdsProtocolConnection.IsUserAllowedToLogon
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection">IWRdsProtocolConnection</a>
 

 


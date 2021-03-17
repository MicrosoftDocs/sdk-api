---
UID: NF:wtsprotocol.IWTSProtocolConnection.IsUserAllowedToLogon
title: IWTSProtocolConnection::IsUserAllowedToLogon (wtsprotocol.h)
description: IWTSProtocolConnection::IsUserAllowedToLogon is no longer available. Instead, use IWRdsProtocolConnection::IsUserAllowedToLogon.
helpviewer_keywords: ["IWTSProtocolConnection interface [Remote Desktop Services]","IsUserAllowedToLogon method","IWTSProtocolConnection.IsUserAllowedToLogon","IWTSProtocolConnection::IsUserAllowedToLogon","IsUserAllowedToLogon","IsUserAllowedToLogon method [Remote Desktop Services]","IsUserAllowedToLogon method [Remote Desktop Services]","IWTSProtocolConnection interface","termserv.iwtsprotocolconnection_isuserallowedtologon","wtsprotocol/IWTSProtocolConnection::IsUserAllowedToLogon"]
old-location: termserv\iwtsprotocolconnection_isuserallowedtologon.htm
tech.root: TermServ
ms.assetid: 297ecc6c-6598-4c1a-94df-9d9924917cdf
ms.date: 12/05/2018
ms.keywords: IWTSProtocolConnection interface [Remote Desktop Services],IsUserAllowedToLogon method, IWTSProtocolConnection.IsUserAllowedToLogon, IWTSProtocolConnection::IsUserAllowedToLogon, IsUserAllowedToLogon, IsUserAllowedToLogon method [Remote Desktop Services], IsUserAllowedToLogon method [Remote Desktop Services],IWTSProtocolConnection interface, termserv.iwtsprotocolconnection_isuserallowedtologon, wtsprotocol/IWTSProtocolConnection::IsUserAllowedToLogon
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWTSProtocolConnection::IsUserAllowedToLogon
 - wtsprotocol/IWTSProtocolConnection::IsUserAllowedToLogon
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wtsprotocol.h
api_name:
 - IWTSProtocolConnection.IsUserAllowedToLogon
---

# IWTSProtocolConnection::IsUserAllowedToLogon


## -description

<p class="CCE_Message">[<b>IWTSProtocolConnection::IsUserAllowedToLogon</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-isuserallowedtologon">IWRdsProtocolConnection::IsUserAllowedToLogon</a>.]

Determines whether a user is allowed to log on to a session.

## -parameters

### -param SessionId [in]

An integer that contains the session ID associated with the user.

### -param UserToken [in]

A pointer to the user token handle.

### -param pDomainName [in]

A pointer to a string that contains the domain name for the user.

### -param pUserName [in]

A pointer to a string that contains the user name.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnection">IWTSProtocolConnection</a>
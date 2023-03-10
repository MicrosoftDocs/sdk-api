---
UID: NF:wtsprotocol.IWTSProtocolConnection.AcceptConnection
title: IWTSProtocolConnection::AcceptConnection (wtsprotocol.h)
description: IWTSProtocolConnection::AcceptConnection is no longer available. Instead, use IWRdsProtocolConnection::AcceptConnection.
helpviewer_keywords: ["AcceptConnection","AcceptConnection method [Remote Desktop Services]","AcceptConnection method [Remote Desktop Services]","IWTSProtocolConnection interface","IWTSProtocolConnection interface [Remote Desktop Services]","AcceptConnection method","IWTSProtocolConnection.AcceptConnection","IWTSProtocolConnection::AcceptConnection","termserv.iwtsprotocolconnection_acceptconnection","wtsprotocol/IWTSProtocolConnection::AcceptConnection"]
old-location: termserv\iwtsprotocolconnection_acceptconnection.htm
tech.root: TermServ
ms.assetid: 5be00911-f68a-410d-8d56-81458b5ff44e
ms.date: 12/05/2018
ms.keywords: AcceptConnection, AcceptConnection method [Remote Desktop Services], AcceptConnection method [Remote Desktop Services],IWTSProtocolConnection interface, IWTSProtocolConnection interface [Remote Desktop Services],AcceptConnection method, IWTSProtocolConnection.AcceptConnection, IWTSProtocolConnection::AcceptConnection, termserv.iwtsprotocolconnection_acceptconnection, wtsprotocol/IWTSProtocolConnection::AcceptConnection
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
 - IWTSProtocolConnection::AcceptConnection
 - wtsprotocol/IWTSProtocolConnection::AcceptConnection
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
 - IWTSProtocolConnection.AcceptConnection
---

# IWTSProtocolConnection::AcceptConnection


## -description

<p class="CCE_Message">[<b>IWTSProtocolConnection::AcceptConnection</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-acceptconnection">IWRdsProtocolConnection::AcceptConnection</a>.]

Directs the protocol to continue with the connection request.



## -remarks

During a connection sequence, the Remote Desktop Services service calls this method after it receives a connection request from a client and after it calls the <a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-sendpolicydata">SendPolicyData</a> method.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnection">IWTSProtocolConnection</a>

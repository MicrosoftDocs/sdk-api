---
UID: NF:wtsprotocol.IWTSProtocolConnection.DisconnectNotify
title: IWTSProtocolConnection::DisconnectNotify (wtsprotocol.h)
description: IWTSProtocolConnection::DisconnectNotify is no longer available. Instead, use IWRdsProtocolConnection::DisconnectNotify.
old-location: termserv\iwtsprotocolconnection_disconnectnotify.htm
tech.root: TermServ
ms.assetid: d2712d53-2e52-49d9-874e-e6425235d3f0
ms.date: 12/05/2018
ms.keywords: DisconnectNotify, DisconnectNotify method [Remote Desktop Services], DisconnectNotify method [Remote Desktop Services],IWTSProtocolConnection interface, IWTSProtocolConnection interface [Remote Desktop Services],DisconnectNotify method, IWTSProtocolConnection.DisconnectNotify, IWTSProtocolConnection::DisconnectNotify, termserv.iwtsprotocolconnection_disconnectnotify, wtsprotocol/IWTSProtocolConnection::DisconnectNotify
f1_keywords:
- wtsprotocol/IWTSProtocolConnection.DisconnectNotify
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Wtsprotocol.h
api_name:
- IWTSProtocolConnection.DisconnectNotify
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWTSProtocolConnection::DisconnectNotify


## -description


<p class="CCE_Message">[<b>IWTSProtocolConnection::DisconnectNotify</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-disconnectnotify">IWRdsProtocolConnection::DisconnectNotify</a>.]

Notifies the protocol that the session has been disconnected.


## -parameters






## -remarks



This is an event notification and you should return immediately from this method. To avoid a possible deadlock, you should not make any function or method calls that will directly or indirectly result in a Remote Desktop Services API being called. If you need to make any outbound call, you should start a new thread and make the outbound call from the new thread.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnection">IWTSProtocolConnection</a>
 

 


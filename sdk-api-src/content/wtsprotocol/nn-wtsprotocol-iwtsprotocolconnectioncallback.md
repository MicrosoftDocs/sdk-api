---
UID: NN:wtsprotocol.IWTSProtocolConnectionCallback
title: IWTSProtocolConnectionCallback (wtsprotocol.h)
description: IWTSProtocolConnectionCallback is no longer available. Instead, use IWRdsProtocolConnectionCallback.
helpviewer_keywords: ["IWTSProtocolConnectionCallback","IWTSProtocolConnectionCallback interface [Remote Desktop Services]","IWTSProtocolConnectionCallback interface [Remote Desktop Services]","described","termserv.iwtsprotocolconnectioncallback","wtsprotocol/IWTSProtocolConnectionCallback"]
old-location: termserv\iwtsprotocolconnectioncallback.htm
tech.root: TermServ
ms.assetid: ac8a2a66-fa1f-48bd-9502-def833e26f31
ms.date: 12/05/2018
ms.keywords: IWTSProtocolConnectionCallback, IWTSProtocolConnectionCallback interface [Remote Desktop Services], IWTSProtocolConnectionCallback interface [Remote Desktop Services],described, termserv.iwtsprotocolconnectioncallback, wtsprotocol/IWTSProtocolConnectionCallback
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
 - IWTSProtocolConnectionCallback
 - wtsprotocol/IWTSProtocolConnectionCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wtsprotocol.h
api_name:
 - IWTSProtocolConnectionCallback
---

# IWTSProtocolConnectionCallback interface


## -description

<p class="CCE_Message">[<b>IWTSProtocolConnectionCallback</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback">IWRdsProtocolConnectionCallback</a>.]

 Exposes methods that provide information about the status of a client connection and that perform actions for the client. This interface is implemented by the Remote Desktop Services service and called by the protocol.

An instance of this interface is associated with a specific instance of the <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnection">IWTSProtocolConnection</a> interface. When the following documentation refers to a connection, it is therefore referring to the specific connection for which the  <b>IWTSProtocolConnection</b> object was created.

## -inheritance

The <b>IWTSProtocolConnectionCallback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWTSProtocolConnectionCallback</b> also has these types of members:


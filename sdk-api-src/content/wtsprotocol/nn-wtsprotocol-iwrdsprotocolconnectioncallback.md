---
UID: NN:wtsprotocol.IWRdsProtocolConnectionCallback
title: IWRdsProtocolConnectionCallback (wtsprotocol.h)
description: Exposes methods that provide information about the status of a client connection and that perform actions for the client. This interface is implemented by the Remote Desktop Services service and called by the protocol.
helpviewer_keywords: ["IWRdsProtocolConnectionCallback","IWRdsProtocolConnectionCallback interface [Remote Desktop Services]","IWRdsProtocolConnectionCallback interface [Remote Desktop Services]","described","termserv.iwrdsprotocolconnectioncallback","wtsprotocol/IWRdsProtocolConnectionCallback"]
old-location: termserv\iwrdsprotocolconnectioncallback.htm
tech.root: TermServ
ms.assetid: 81a73688-f39e-4960-8587-602d56c11e7e
ms.date: 12/05/2018
ms.keywords: IWRdsProtocolConnectionCallback, IWRdsProtocolConnectionCallback interface [Remote Desktop Services], IWRdsProtocolConnectionCallback interface [Remote Desktop Services],described, termserv.iwrdsprotocolconnectioncallback, wtsprotocol/IWRdsProtocolConnectionCallback
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWRdsProtocolConnectionCallback
 - wtsprotocol/IWRdsProtocolConnectionCallback
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
 - IWRdsProtocolConnectionCallback
---

# IWRdsProtocolConnectionCallback interface


## -description

Exposes methods that provide information about the status of a client connection and that perform actions for the client. This interface is implemented by the Remote Desktop Services service and called by the protocol.

An instance of this interface is associated with a specific instance of the <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection">IWRdsProtocolConnection</a> interface. When the following documentation refers to a connection, it is therefore referring to the specific connection for which the  <b>IWRdsProtocolConnection</b> object was created.

## -inheritance

The <b>IWRdsProtocolConnectionCallback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWRdsProtocolConnectionCallback</b> also has these types of members:

## -remarks

To avoid a possible deadlock when calling any of the methods on this interface, you should not make any function or method calls that will directly or indirectly result in a Remote Desktop Services API being called. If you need to make any outbound call, you should start a new thread and make the outbound call from the new thread.

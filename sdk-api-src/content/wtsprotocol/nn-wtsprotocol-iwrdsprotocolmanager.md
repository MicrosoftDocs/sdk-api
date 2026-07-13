---
UID: NN:wtsprotocol.IWRdsProtocolManager
title: IWRdsProtocolManager (wtsprotocol.h)
description: Exposes methods that the Remote Desktop Services service uses to communicate with the protocol provider.
helpviewer_keywords: ["IWRdsProtocolManager","IWRdsProtocolManager interface [Remote Desktop Services]","IWRdsProtocolManager interface [Remote Desktop Services]","described","termserv.iwrdsprotocolmanager","wtsprotocol/IWRdsProtocolManager"]
old-location: termserv\iwrdsprotocolmanager.htm
tech.root: TermServ
ms.assetid: 626d579a-88a2-4f72-9d91-b27e517b4806
ms.date: 12/05/2018
ms.keywords: IWRdsProtocolManager, IWRdsProtocolManager interface [Remote Desktop Services], IWRdsProtocolManager interface [Remote Desktop Services],described, termserv.iwrdsprotocolmanager, wtsprotocol/IWRdsProtocolManager
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
 - IWRdsProtocolManager
 - wtsprotocol/IWRdsProtocolManager
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
 - IWRdsProtocolManager
---

# IWRdsProtocolManager interface


## -description

Exposes methods that  the Remote Desktop Services service uses to communicate with the protocol provider. It is the only interface in the protocol provider for which the Remote Desktop Services service calls <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex">CoCreateInstanceEx</a>. In addition, the first call the Remote Desktop Services service makes into the protocol provider is to the <a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener">CreateListener</a> method.

## -inheritance

The <b>IWRdsProtocolManager</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWRdsProtocolManager</b> also has these types of members:

## -remarks

To avoid a possible deadlock when calling any of the methods on this interface, you should not make any function or method calls that will directly or indirectly result in a Remote Desktop Services API being called. If you need to make any outbound call, you should start a new thread and make the outbound call from the new thread.

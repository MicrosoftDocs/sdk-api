---
UID: NN:wtsprotocol.IWRdsProtocolShadowCallback
title: IWRdsProtocolShadowCallback (wtsprotocol.h)
description: Exposes methods called by the protocol to notify the Remote Desktop Services service to start or stop the target side of a shadow.
helpviewer_keywords: ["IWRdsProtocolShadowCallback","IWRdsProtocolShadowCallback interface [Remote Desktop Services]","IWRdsProtocolShadowCallback interface [Remote Desktop Services]","described","termserv.iwrdsprotocolshadowcallback","wtsprotocol/IWRdsProtocolShadowCallback"]
old-location: termserv\iwrdsprotocolshadowcallback.htm
tech.root: TermServ
ms.assetid: 47727d33-df3d-49da-bc82-a4ed5ce0a381
ms.date: 12/05/2018
ms.keywords: IWRdsProtocolShadowCallback, IWRdsProtocolShadowCallback interface [Remote Desktop Services], IWRdsProtocolShadowCallback interface [Remote Desktop Services],described, termserv.iwrdsprotocolshadowcallback, wtsprotocol/IWRdsProtocolShadowCallback
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
 - IWRdsProtocolShadowCallback
 - wtsprotocol/IWRdsProtocolShadowCallback
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
 - IWRdsProtocolShadowCallback
---

# IWRdsProtocolShadowCallback interface


## -description

 Exposes methods called by the protocol to notify the Remote Desktop Services service to start or stop the target side of a shadow. This interface is the callback interface for the <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowconnection">IWRdsProtocolShadowConnection</a> interface. It is implemented by the Remote Desktop Services service and called by the protocol provider.

## -inheritance

The <b>IWRdsProtocolShadowCallback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWRdsProtocolShadowCallback</b> also has these types of members:


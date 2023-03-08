---
UID: NN:wtsprotocol.IWRdsProtocolShadowConnection
title: IWRdsProtocolShadowConnection (wtsprotocol.h)
description: Exposes methods that notify the protocol provider about the status of session shadowing.
helpviewer_keywords: ["IWRdsProtocolShadowConnection","IWRdsProtocolShadowConnection interface [Remote Desktop Services]","IWRdsProtocolShadowConnection interface [Remote Desktop Services]","described","termserv.iwrdsprotocolshadowconnection","wtsprotocol/IWRdsProtocolShadowConnection"]
old-location: termserv\iwrdsprotocolshadowconnection.htm
tech.root: TermServ
ms.assetid: d23c4902-4e61-45ff-8a49-62eea1b92d4a
ms.date: 12/05/2018
ms.keywords: IWRdsProtocolShadowConnection, IWRdsProtocolShadowConnection interface [Remote Desktop Services], IWRdsProtocolShadowConnection interface [Remote Desktop Services],described, termserv.iwrdsprotocolshadowconnection, wtsprotocol/IWRdsProtocolShadowConnection
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
 - IWRdsProtocolShadowConnection
 - wtsprotocol/IWRdsProtocolShadowConnection
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
 - IWRdsProtocolShadowConnection
---

# IWRdsProtocolShadowConnection interface


## -description

Exposes methods that notify the protocol provider about the status of session shadowing. The <b>IWRdsProtocolShadowConnection</b> interface can also be used to exchange information between the shadow client and the shadow target. This interface is implemented by the protocol provider, and its methods are called by the Remote Desktop Services service.

## -inheritance

The <b>IWRdsProtocolShadowConnection</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWRdsProtocolShadowConnection</b> also has these types of members:


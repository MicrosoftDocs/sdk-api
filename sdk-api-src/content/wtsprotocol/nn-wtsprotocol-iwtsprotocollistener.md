---
UID: NN:wtsprotocol.IWTSProtocolListener
title: IWTSProtocolListener (wtsprotocol.h)
description: IWTSProtocolListener is no longer available. Instead, use IWRdsProtocolListener.
helpviewer_keywords: ["IWTSProtocolListener","IWTSProtocolListener interface [Remote Desktop Services]","IWTSProtocolListener interface [Remote Desktop Services]","described","termserv.iwtsprotocollistener","wtsprotocol/IWTSProtocolListener"]
old-location: termserv\iwtsprotocollistener.htm
tech.root: TermServ
ms.assetid: b11eb19f-ffc3-4a68-85c6-90a2412168f8
ms.date: 12/05/2018
ms.keywords: IWTSProtocolListener, IWTSProtocolListener interface [Remote Desktop Services], IWTSProtocolListener interface [Remote Desktop Services],described, termserv.iwtsprotocollistener, wtsprotocol/IWTSProtocolListener
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
 - IWTSProtocolListener
 - wtsprotocol/IWTSProtocolListener
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
 - IWTSProtocolListener
---

# IWTSProtocolListener interface


## -description

<p class="CCE_Message">[<b>IWTSProtocolListener</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener">IWRdsProtocolListener</a>.]

Exposes methods that request that the protocol start and stop listening for client connection requests. The interface is implemented by the protocol and its methods are called by the Remote Desktop Services service.

## -inheritance

The <b>IWTSProtocolListener</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWTSProtocolListener</b> also has these types of members:


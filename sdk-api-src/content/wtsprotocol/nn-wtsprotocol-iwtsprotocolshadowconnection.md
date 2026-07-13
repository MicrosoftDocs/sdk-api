---
UID: NN:wtsprotocol.IWTSProtocolShadowConnection
title: IWTSProtocolShadowConnection (wtsprotocol.h)
description: IWTSProtocolShadowConnection is no longer available. Instead, use IWRdsProtocolShadowConnection.
helpviewer_keywords: ["IWTSProtocolShadowConnection","IWTSProtocolShadowConnection interface [Remote Desktop Services]","IWTSProtocolShadowConnection interface [Remote Desktop Services]","described","termserv.iwtsprotocolshadowconnection","wtsprotocol/IWTSProtocolShadowConnection"]
old-location: termserv\iwtsprotocolshadowconnection.htm
tech.root: TermServ
ms.assetid: 83285a6a-903f-4c23-8f62-b04bbeaa52f9
ms.date: 12/05/2018
ms.keywords: IWTSProtocolShadowConnection, IWTSProtocolShadowConnection interface [Remote Desktop Services], IWTSProtocolShadowConnection interface [Remote Desktop Services],described, termserv.iwtsprotocolshadowconnection, wtsprotocol/IWTSProtocolShadowConnection
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
 - IWTSProtocolShadowConnection
 - wtsprotocol/IWTSProtocolShadowConnection
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
 - IWTSProtocolShadowConnection
---

# IWTSProtocolShadowConnection interface


## -description

<p class="CCE_Message">[<b>IWTSProtocolShadowConnection</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowconnection">IWRdsProtocolShadowConnection</a>.]

Exposes methods that notify the protocol provider about the status of session shadowing. The <b>IWTSProtocolShadowConnection</b> interface can also be used to exchange information between the shadow client and the shadow target. This interface is implemented by the protocol provider, and its methods are called by the Remote Desktop Services service.

## -inheritance

The <b>IWTSProtocolShadowConnection</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWTSProtocolShadowConnection</b> also has these types of members:


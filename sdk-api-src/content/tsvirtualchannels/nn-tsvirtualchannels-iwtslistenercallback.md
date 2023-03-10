---
UID: NN:tsvirtualchannels.IWTSListenerCallback
title: IWTSListenerCallback (tsvirtualchannels.h)
description: Used to notify the Remote Desktop Connection (RDC) client plug-in about incoming requests on a particular listener.
helpviewer_keywords: ["IWTSListenerCallback","IWTSListenerCallback interface [Remote Desktop Services]","IWTSListenerCallback interface [Remote Desktop Services]","described","termserv.iwtslistenercallback","tsvirtualchannels/IWTSListenerCallback"]
old-location: termserv\iwtslistenercallback.htm
tech.root: TermServ
ms.assetid: b5f1d74d-31e6-4447-82ab-6dd3ad9957fd
ms.date: 12/05/2018
ms.keywords: IWTSListenerCallback, IWTSListenerCallback interface [Remote Desktop Services], IWTSListenerCallback interface [Remote Desktop Services],described, termserv.iwtslistenercallback, tsvirtualchannels/IWTSListenerCallback
req.header: tsvirtualchannels.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: TsVirtualChannels.idl
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
 - IWTSListenerCallback
 - tsvirtualchannels/IWTSListenerCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - TsVirtualChannels.h
api_name:
 - IWTSListenerCallback
---

# IWTSListenerCallback interface


## -description

Used to notify the Remote Desktop Connection (RDC) client plug-in about incoming requests  on a particular listener.

This interface is implemented by the Remote Desktop Connection (RDC) client plug-in. Calls will always be made on the same thread, with the exception of an out-of-process plug-in, where the calls will arrive on a remote procedure call (RPC) thread pool.
Implementation should not block these calls because this may block other incoming connections or data on existing connections.

## -inheritance

The <b>IWTSListenerCallback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWTSListenerCallback</b> also has these types of members:

## -see-also

<a href="/windows/desktop/TermServ/dvc-client-plug-in-example">DVC Client Plug-in Example</a>

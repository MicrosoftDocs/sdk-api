---
UID: NN:tsvirtualchannels.IWTSBitmapRendererCallback
title: IWTSBitmapRendererCallback (tsvirtualchannels.h)
description: A dynamic virtual channel plug-in implements this interface to be notified when the size of the rendering area changes.
helpviewer_keywords: ["IWTSBitmapRendererCallback","IWTSBitmapRendererCallback interface [Remote Desktop Services]","IWTSBitmapRendererCallback interface [Remote Desktop Services]","described","termserv.iwtsbitmaprenderercallback","tsvirtualchannels/IWTSBitmapRendererCallback"]
old-location: termserv\iwtsbitmaprenderercallback.htm
tech.root: TermServ
ms.assetid: bdb8280b-6ebc-47e4-9789-47e3bda96efc
ms.date: 12/05/2018
ms.keywords: IWTSBitmapRendererCallback, IWTSBitmapRendererCallback interface [Remote Desktop Services], IWTSBitmapRendererCallback interface [Remote Desktop Services],described, termserv.iwtsbitmaprenderercallback, tsvirtualchannels/IWTSBitmapRendererCallback
req.header: tsvirtualchannels.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: TSVirtualChannels.idl
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
 - IWTSBitmapRendererCallback
 - tsvirtualchannels/IWTSBitmapRendererCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tsvirtualchannels.h
api_name:
 - IWTSBitmapRendererCallback
---

# IWTSBitmapRendererCallback interface


## -description

A dynamic virtual channel plug-in implements this interface to be notified when the size of  the rendering area changes. A pointer to this interface is provided to the rendering service by using the <a href="/windows/desktop/api/tsvirtualchannels/nf-tsvirtualchannels-iwtsbitmaprenderservice-getmappedrenderer">IWTSBitmapRenderService::GetMappedRenderer</a> method.

## -inheritance

The <b>IWTSBitmapRendererCallback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWTSBitmapRendererCallback</b> also has these types of members:


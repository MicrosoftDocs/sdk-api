---
UID: NF:tsvirtualchannels.IWTSBitmapRendererCallback.OnTargetSizeChanged
title: IWTSBitmapRendererCallback::OnTargetSizeChanged (tsvirtualchannels.h)
description: Called when the size of the render target has changed.
helpviewer_keywords: ["IWTSBitmapRendererCallback interface [Remote Desktop Services]","OnTargetSizeChanged method","IWTSBitmapRendererCallback.OnTargetSizeChanged","IWTSBitmapRendererCallback::OnTargetSizeChanged","OnTargetSizeChanged","OnTargetSizeChanged method [Remote Desktop Services]","OnTargetSizeChanged method [Remote Desktop Services]","IWTSBitmapRendererCallback interface","termserv.iwtsbitmaprenderercallback_ontargetsizechanged","tsvirtualchannels/IWTSBitmapRendererCallback::OnTargetSizeChanged"]
old-location: termserv\iwtsbitmaprenderercallback_ontargetsizechanged.htm
tech.root: TermServ
ms.assetid: 2c4eeec8-7d9c-4321-9fdb-3ea8c7a36893
ms.date: 12/05/2018
ms.keywords: IWTSBitmapRendererCallback interface [Remote Desktop Services],OnTargetSizeChanged method, IWTSBitmapRendererCallback.OnTargetSizeChanged, IWTSBitmapRendererCallback::OnTargetSizeChanged, OnTargetSizeChanged, OnTargetSizeChanged method [Remote Desktop Services], OnTargetSizeChanged method [Remote Desktop Services],IWTSBitmapRendererCallback interface, termserv.iwtsbitmaprenderercallback_ontargetsizechanged, tsvirtualchannels/IWTSBitmapRendererCallback::OnTargetSizeChanged
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
 - IWTSBitmapRendererCallback::OnTargetSizeChanged
 - tsvirtualchannels/IWTSBitmapRendererCallback::OnTargetSizeChanged
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
 - IWTSBitmapRendererCallback.OnTargetSizeChanged
---

# IWTSBitmapRendererCallback::OnTargetSizeChanged


## -description

Called when the size of the render target has changed. The image passed to <a href="/windows/desktop/api/tsvirtualchannels/nf-tsvirtualchannels-iwtsbitmaprenderer-render">IWTSBitmapRenderer::Render</a> must conform to this size.

## -parameters

### -param rcNewSize [in]

A <b>RECT</b> structure that contains the new size of the render target.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tsvirtualchannels/nn-tsvirtualchannels-iwtsbitmaprenderercallback">IWTSBitmapRendererCallback</a>
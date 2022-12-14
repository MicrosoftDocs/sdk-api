---
UID: NF:tsvirtualchannels.IWTSBitmapRenderer.Render
title: IWTSBitmapRenderer::Render (tsvirtualchannels.h)
description: Called by a dynamic virtual channel plug-in to render bitmaps.
helpviewer_keywords: ["IWTSBitmapRenderer interface [Remote Desktop Services]","Render method","IWTSBitmapRenderer.Render","IWTSBitmapRenderer::Render","Render","Render method [Remote Desktop Services]","Render method [Remote Desktop Services]","IWTSBitmapRenderer interface","termserv.iwtsbitmaprenderer_render","tsvirtualchannels/IWTSBitmapRenderer::Render"]
old-location: termserv\iwtsbitmaprenderer_render.htm
tech.root: TermServ
ms.assetid: 536c6954-0cde-48d1-ba5b-a97c9942f0f6
ms.date: 12/05/2018
ms.keywords: IWTSBitmapRenderer interface [Remote Desktop Services],Render method, IWTSBitmapRenderer.Render, IWTSBitmapRenderer::Render, Render, Render method [Remote Desktop Services], Render method [Remote Desktop Services],IWTSBitmapRenderer interface, termserv.iwtsbitmaprenderer_render, tsvirtualchannels/IWTSBitmapRenderer::Render
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
 - IWTSBitmapRenderer::Render
 - tsvirtualchannels/IWTSBitmapRenderer::Render
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
 - IWTSBitmapRenderer.Render
---

# IWTSBitmapRenderer::Render


## -description

Called by a dynamic virtual channel plug-in to render bitmaps.

## -parameters

### -param imageFormat [in]

Specifies the format of the data in the <i>pImageBuffer</i> buffer. This parameter is ignored and only bitmaps can be rendered.

### -param dwWidth [in]

The width of the bitmap.

### -param dwHeight [in]

The height of the bitmap.

### -param cbStride [in]

The stride width of the bitmap.

### -param cbImageBuffer [in]

The size, in bytes, of the <i>pImageBuffer</i> buffer.

### -param pImageBuffer [in]

An array of bytes that contains the data to render.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tsvirtualchannels/nn-tsvirtualchannels-iwtsbitmaprenderer">IWTSBitmapRenderer</a>
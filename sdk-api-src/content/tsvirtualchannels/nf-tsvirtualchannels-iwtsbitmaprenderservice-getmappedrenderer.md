---
UID: NF:tsvirtualchannels.IWTSBitmapRenderService.GetMappedRenderer
title: IWTSBitmapRenderService::GetMappedRenderer (tsvirtualchannels.h)
description: Obtains the bitmap rendering object used to render media on the server.
helpviewer_keywords: ["GetMappedRenderer","GetMappedRenderer method [Remote Desktop Services]","GetMappedRenderer method [Remote Desktop Services]","IWTSBitmapRenderService interface","IWTSBitmapRenderService interface [Remote Desktop Services]","GetMappedRenderer method","IWTSBitmapRenderService.GetMappedRenderer","IWTSBitmapRenderService::GetMappedRenderer","termserv.iwtsbitmaprenderservice_getmappedrenderer","tsvirtualchannels/IWTSBitmapRenderService::GetMappedRenderer"]
old-location: termserv\iwtsbitmaprenderservice_getmappedrenderer.htm
tech.root: TermServ
ms.assetid: 1a5f8ddb-eaf6-4138-8bb7-4d513aff88b5
ms.date: 12/05/2018
ms.keywords: GetMappedRenderer, GetMappedRenderer method [Remote Desktop Services], GetMappedRenderer method [Remote Desktop Services],IWTSBitmapRenderService interface, IWTSBitmapRenderService interface [Remote Desktop Services],GetMappedRenderer method, IWTSBitmapRenderService.GetMappedRenderer, IWTSBitmapRenderService::GetMappedRenderer, termserv.iwtsbitmaprenderservice_getmappedrenderer, tsvirtualchannels/IWTSBitmapRenderService::GetMappedRenderer
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
 - IWTSBitmapRenderService::GetMappedRenderer
 - tsvirtualchannels/IWTSBitmapRenderService::GetMappedRenderer
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
 - IWTSBitmapRenderService.GetMappedRenderer
---

# IWTSBitmapRenderService::GetMappedRenderer


## -description

Obtains the bitmap rendering object used to render media on the server.

## -parameters

### -param mappingId [in]

A 64-bit number that uniquely identifies the render mapping.

### -param pMappedRendererCallback [in]

The address of the caller's <a href="/windows/desktop/api/tsvirtualchannels/nn-tsvirtualchannels-iwtsbitmaprenderercallback">IWTSBitmapRendererCallback</a> interface.

### -param ppMappedRenderer [out]

The address of an <a href="/windows/desktop/api/tsvirtualchannels/nn-tsvirtualchannels-iwtsbitmaprenderer">IWTSBitmapRenderer</a> interface pointer that receives the bitmap renderer. When you have finished using pointer, release it by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release()</a> method.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tsvirtualchannels/nn-tsvirtualchannels-iwtsbitmaprenderservice">IWTSBitmapRenderService</a>
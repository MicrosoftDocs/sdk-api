---
UID: NF:mfmediaengine.IMFMediaEngineSupportsSourceTransfer.DetachMediaSource
title: IMFMediaEngineSupportsSourceTransfer::DetachMediaSource (mfmediaengine.h)
description: Detaches the media source.
helpviewer_keywords: ["DetachMediaSource","DetachMediaSource method [Media Foundation]","DetachMediaSource method [Media Foundation]","IMFMediaEngineSupportsSourceTransfer interface","IMFMediaEngineSupportsSourceTransfer interface [Media Foundation]","DetachMediaSource method","IMFMediaEngineSupportsSourceTransfer.DetachMediaSource","IMFMediaEngineSupportsSourceTransfer::DetachMediaSource","mf.imfmediaenginesupportssourcetransfer_detachmediasource","mfmediaengine/IMFMediaEngineSupportsSourceTransfer::DetachMediaSource"]
old-location: mf\imfmediaenginesupportssourcetransfer_detachmediasource.htm
tech.root: mf
ms.assetid: a085fc53-91a3-46bb-862c-dde16fb7fa42
ms.date: 12/05/2018
ms.keywords: DetachMediaSource, DetachMediaSource method [Media Foundation], DetachMediaSource method [Media Foundation],IMFMediaEngineSupportsSourceTransfer interface, IMFMediaEngineSupportsSourceTransfer interface [Media Foundation],DetachMediaSource method, IMFMediaEngineSupportsSourceTransfer.DetachMediaSource, IMFMediaEngineSupportsSourceTransfer::DetachMediaSource, mf.imfmediaenginesupportssourcetransfer_detachmediasource, mfmediaengine/IMFMediaEngineSupportsSourceTransfer::DetachMediaSource
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfmediaengine.idl
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
 - IMFMediaEngineSupportsSourceTransfer::DetachMediaSource
 - mfmediaengine/IMFMediaEngineSupportsSourceTransfer::DetachMediaSource
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngineSupportsSourceTransfer.DetachMediaSource
---

# IMFMediaEngineSupportsSourceTransfer::DetachMediaSource


## -description

Detaches the media source.

## -parameters

### -param ppByteStream [out]

Receives the byte stream.

### -param ppMediaSource [out]

Receives the media source.

### -param ppMSE [out]

Receives the media source extension.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginesupportssourcetransfer">IMFMediaEngineSupportsSourceTransfer</a>
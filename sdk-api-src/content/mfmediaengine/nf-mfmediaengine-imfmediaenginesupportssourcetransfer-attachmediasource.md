---
UID: NF:mfmediaengine.IMFMediaEngineSupportsSourceTransfer.AttachMediaSource
title: IMFMediaEngineSupportsSourceTransfer::AttachMediaSource (mfmediaengine.h)
description: Attaches the media source.
helpviewer_keywords: ["AttachMediaSource","AttachMediaSource method [Media Foundation]","AttachMediaSource method [Media Foundation]","IMFMediaEngineSupportsSourceTransfer interface","IMFMediaEngineSupportsSourceTransfer interface [Media Foundation]","AttachMediaSource method","IMFMediaEngineSupportsSourceTransfer.AttachMediaSource","IMFMediaEngineSupportsSourceTransfer::AttachMediaSource","mf.imfmediaenginesupportssourcetransfer_attachmediasource","mfmediaengine/IMFMediaEngineSupportsSourceTransfer::AttachMediaSource"]
old-location: mf\imfmediaenginesupportssourcetransfer_attachmediasource.htm
tech.root: mf
ms.assetid: db7c17cf-020d-4317-801e-35539e25df49
ms.date: 12/05/2018
ms.keywords: AttachMediaSource, AttachMediaSource method [Media Foundation], AttachMediaSource method [Media Foundation],IMFMediaEngineSupportsSourceTransfer interface, IMFMediaEngineSupportsSourceTransfer interface [Media Foundation],AttachMediaSource method, IMFMediaEngineSupportsSourceTransfer.AttachMediaSource, IMFMediaEngineSupportsSourceTransfer::AttachMediaSource, mf.imfmediaenginesupportssourcetransfer_attachmediasource, mfmediaengine/IMFMediaEngineSupportsSourceTransfer::AttachMediaSource
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
 - IMFMediaEngineSupportsSourceTransfer::AttachMediaSource
 - mfmediaengine/IMFMediaEngineSupportsSourceTransfer::AttachMediaSource
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
 - IMFMediaEngineSupportsSourceTransfer.AttachMediaSource
---

# IMFMediaEngineSupportsSourceTransfer::AttachMediaSource


## -description

Attaches the media source.

## -parameters

### -param pByteStream [in]

Specifies the byte stream.

### -param pMediaSource [in]

Specifies the media source.

### -param pMSE [in]

Specifies the media source extension.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginesupportssourcetransfer">IMFMediaEngineSupportsSourceTransfer</a>
---
UID: NF:mfidl.MFCreateAVIMediaSink
title: MFCreateAVIMediaSink function (mfidl.h)
description: Creates an Audio-Video Interleaved (AVI) Sink.
helpviewer_keywords: ["MFCreateAVIMediaSink","MFCreateAVIMediaSink function [Media Foundation]","mf.mfcreateavimediasink","mfidl/MFCreateAVIMediaSink"]
old-location: mf\mfcreateavimediasink.htm
tech.root: mf
ms.assetid: BAF47469-783B-4035-BD83-2921A88877E4
ms.date: 12/05/2018
ms.keywords: MFCreateAVIMediaSink, MFCreateAVIMediaSink function [Media Foundation], mf.mfcreateavimediasink, mfidl/MFCreateAVIMediaSink
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: mfsrcsnk.lib
req.dll: mfsrcsnk.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreateAVIMediaSink
 - mfidl/MFCreateAVIMediaSink
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfsrcsnk.dll
api_name:
 - MFCreateAVIMediaSink
---

# MFCreateAVIMediaSink function


## -description

Creates an Audio-Video Interleaved (AVI) Sink.

## -parameters

### -param pIByteStream [in]

Pointer to the byte stream that will be used to write the AVI file.

### -param pVideoMediaType [in]

Pointer to the media type of the video input stream

### -param pAudioMediaType [in, optional]

Pointer to the media type of the audio input stream

### -param ppIMediaSink [out]

Receives a pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasink">IMFMediaSink</a> Interface.  The caller must release this interface.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
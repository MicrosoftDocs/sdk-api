---
UID: NF:mfidl.MFCreateMPEG4MediaSink
title: MFCreateMPEG4MediaSink function (mfidl.h)
description: Creates a media sink for authoring MP4 files.
helpviewer_keywords: ["MFCreateMPEG4MediaSink","MFCreateMPEG4MediaSink function [Media Foundation]","mf.mfcreatempeg4mediasink","mfidl/MFCreateMPEG4MediaSink"]
old-location: mf\mfcreatempeg4mediasink.htm
tech.root: mf
ms.assetid: e2a7c596-98b1-4c36-ba83-534459b22690
ms.date: 12/05/2018
ms.keywords: MFCreateMPEG4MediaSink, MFCreateMPEG4MediaSink function [Media Foundation], mf.mfcreatempeg4mediasink, mfidl/MFCreateMPEG4MediaSink
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreateMPEG4MediaSink
 - mfidl/MFCreateMPEG4MediaSink
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFCreateMPEG4MediaSink
---

# MFCreateMPEG4MediaSink function


## -description

Creates a media sink for authoring MP4 files.

## -parameters

### -param pIByteStream [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a> interface of a byte stream.  The media sink writes the MP4 file to this byte stream. The byte stream must be writable and support seeking.

### -param pVideoMediaType [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface of a video media type. This type specifies the format of the video stream.

This parameter can be <b>NULL</b>, but not if <i>pAudioMediaType</i> is <b>NULL</b>.

### -param pAudioMediaType [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface of an audio media type. This type specifies the format of the audio stream.

This parameter can be <b>NULL</b>, but not if <i>pVideoMediaType</i> is <b>NULL</b>.

### -param ppIMediaSink [out]

Receives a pointer to the MP4 media sink's <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasink">IMFMediaSink</a> interface. The caller must release the interface.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The MP4 media sink supports a maximum of one video stream and one audio stream. The initial stream formats are given in the <i>pVideoMediaType</i> and <i>pAudioMediaType</i> parameters. To create an MP4 file with one stream, set the other stream type to <b>NULL</b>. For example, to create an audio-only file, set <i>pVideoMediaType</i> to <b>NULL</b>. 

The number of streams is fixed when you create the media sink. The sink does not support the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink">IMFMediaSink::AddStreamSink</a> method.

To author 3GP files, use the <a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreate3gpmediasink">MFCreate3GPMediaSink</a> function.

## -see-also

<a href="/windows/desktop/medfound/mpeg-4-file-sink">MPEG-4 File Sink</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
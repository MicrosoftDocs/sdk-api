---
UID: NF:mfidl.MFCreate3GPMediaSink
title: MFCreate3GPMediaSink function (mfidl.h)
description: Creates a media sink for authoring 3GP files.
helpviewer_keywords: ["MFCreate3GPMediaSink","MFCreate3GPMediaSink function [Media Foundation]","mf.mfcreate3gpmediasink","mfidl/MFCreate3GPMediaSink"]
old-location: mf\mfcreate3gpmediasink.htm
tech.root: mf
ms.assetid: a0a1f6af-5d73-4347-abd7-9b2bde61fdf2
ms.date: 12/05/2018
ms.keywords: MFCreate3GPMediaSink, MFCreate3GPMediaSink function [Media Foundation], mf.mfcreate3gpmediasink, mfidl/MFCreate3GPMediaSink
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
 - MFCreate3GPMediaSink
 - mfidl/MFCreate3GPMediaSink
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
 - MFCreate3GPMediaSink
---

# MFCreate3GPMediaSink function


## -description

Creates a media sink for authoring 3GP files.

## -parameters

### -param pIByteStream [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a> interface of a byte stream.  The media sink writes the 3GP file to this byte stream. The byte stream must be writable and support seeking.

### -param pVideoMediaType [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface of a video media type. This type specifies the format of the video stream.

This parameter can be <b>NULL</b>, but not if <i>pAudioMediaType</i> is <b>NULL</b>.

### -param pAudioMediaType [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface of an audio media type. This type specifies the format of the audio stream.

This parameter can be <b>NULL</b>, but not if <i>pVideoMediaType</i> is <b>NULL</b>.

### -param ppIMediaSink [out]

Receives a pointer to the 3GP media sink's <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasink">IMFMediaSink</a> interface. The caller must release the interface.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The 3GP media sink supports a maximum of one video stream and one audio stream. The initial stream formats are given in the <i>pVideoMediaType</i> and <i>pAudioMediaType</i> parameters. To create an MP4 file with one stream, set the other stream type to <b>NULL</b>. For example, to create an audio-only file, set <i>pVideoMediaType</i> to <b>NULL</b>. 

The number of streams is fixed when you create the media sink. The sink does not support the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink">IMFMediaSink::AddStreamSink</a> method.

To author MP4 files, use the <a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreatempeg4mediasink">MFCreateMPEG4MediaSink</a> function.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
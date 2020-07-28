---
UID: NF:mfidl.MFCreateFMPEG4MediaSink
title: MFCreateFMPEG4MediaSink function (mfidl.h)
description: Creates a media sink for authoring fragmented MP4 files.
helpviewer_keywords: ["MFCreateFMPEG4MediaSink","MFCreateFMPEG4MediaSink function [Media Foundation]","mf.mfcreatefmpeg4mediasink","mfidl/MFCreateFMPEG4MediaSink"]
old-location: mf\mfcreatefmpeg4mediasink.htm
tech.root: mf
ms.assetid: 31FDA8BD-C837-4CA4-8635-D4A7B53AC7AC
ms.date: 12/05/2018
ms.keywords: MFCreateFMPEG4MediaSink, MFCreateFMPEG4MediaSink function [Media Foundation], mf.mfcreatefmpeg4mediasink, mfidl/MFCreateFMPEG4MediaSink
f1_keywords:
- mfidl/MFCreateFMPEG4MediaSink
dev_langs:
- c++
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: None supported
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- mf.dll
api_name:
- MFCreateFMPEG4MediaSink
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MFCreateFMPEG4MediaSink function


## -description


Creates a media sink for authoring fragmented MP4 files.


## -parameters




### -param pIByteStream [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a> interface of a byte stream.  The media sink writes the MP4 file to this byte stream. The byte stream must be writable and support seeking.


### -param pVideoMediaType [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface of a video media type. This type specifies the format of the video stream.

This parameter can be <b>NULL</b>, but not if <i>pAudioMediaType</i> is <b>NULL</b>.


### -param pAudioMediaType [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface of an audio media type. This type specifies the format of the audio stream.

This parameter can be <b>NULL</b>, but not if <i>pVideoMediaType</i> is <b>NULL</b>.


### -param ppIMediaSink [out]

Receives a pointer to the MP4 media sink's <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfmediasink">IMFMediaSink</a> interface. The caller must release the interface.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
 

 


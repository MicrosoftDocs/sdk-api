---
UID: NF:mfidl.MFCreateTranscodeTopologyFromByteStream
title: MFCreateTranscodeTopologyFromByteStream function (mfidl.h)
description: Creates a topology for transcoding to a byte stream.
helpviewer_keywords: ["MFCreateTranscodeTopologyFromByteStream","MFCreateTranscodeTopologyFromByteStream function [Media Foundation]","mf.mfcreatetranscodetopologyfrombytestream","mfidl/MFCreateTranscodeTopologyFromByteStream"]
old-location: mf\mfcreatetranscodetopologyfrombytestream.htm
tech.root: mf
ms.assetid: FBA9E0A1-7763-4566-8245-D626C82D0355
ms.date: 12/05/2018
ms.keywords: MFCreateTranscodeTopologyFromByteStream, MFCreateTranscodeTopologyFromByteStream function [Media Foundation], mf.mfcreatetranscodetopologyfrombytestream, mfidl/MFCreateTranscodeTopologyFromByteStream
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - MFCreateTranscodeTopologyFromByteStream
 - mfidl/MFCreateTranscodeTopologyFromByteStream
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
 - MFCreateTranscodeTopologyFromByteStream
---

# MFCreateTranscodeTopologyFromByteStream function


## -description

Creates a topology for transcoding to a byte stream.

## -parameters

### -param pSrc [in]

A pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasource">IMFMediaSource</a> interface of a media source. The media source provides that source content for transcoding.

### -param pOutputStream [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a> interface of a byte stream. The transcoded output will be written to this byte stream.

### -param pProfile [in]

A pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile">IMFTranscodeProfile</a> interface of a transcoding profile.

### -param ppTranscodeTopo [out]

Receives a pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imftopology">IMFTopology</a> interface. The caller must release the interface.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function creates a partial topology that contains the media source, the encoder, and the media sink.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/media-session">Media Session</a>



<a href="/windows/desktop/medfound/topologies">Topologies</a>
---
UID: NF:mfidl.MFCreateADTSMediaSink
title: MFCreateADTSMediaSink function (mfidl.h)
description: Creates an instance of the audio data transport stream (ADTS) media sink.
helpviewer_keywords: ["MFCreateADTSMediaSink","MFCreateADTSMediaSink function [Media Foundation]","mf.mfcreateadtsmediasink","mfidl/MFCreateADTSMediaSink"]
old-location: mf\mfcreateadtsmediasink.htm
tech.root: mf
ms.assetid: 18B2F5C7-61A6-447B-9BC8-2394A68BA777
ms.date: 12/05/2018
ms.keywords: MFCreateADTSMediaSink, MFCreateADTSMediaSink function [Media Foundation], mf.mfcreateadtsmediasink, mfidl/MFCreateADTSMediaSink
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
 - MFCreateADTSMediaSink
 - mfidl/MFCreateADTSMediaSink
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
 - MFCreateADTSMediaSink
---

# MFCreateADTSMediaSink function


## -description

Creates an instance of the audio data transport stream (ADTS) media sink.

## -parameters

### -param pTargetByteStream [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a> interface of a byte stream. The media sink writes the ADTS stream to this byte stream. The byte stream must be writable.

### -param pAudioMediaType [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface. This parameter specifies the media type for the ADTS stream. The media type must contain the following attributes.

<table>
<tr>
<th>Attribute</th>
<th>Value</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/medfound/mf-mt-major-type-attribute">MF_MT_MAJOR_TYPE</a>
</td>
<td><b>MFMediaType_Audio</b></td>
</tr>
<tr>
<td>
<a href="/windows/desktop/medfound/mf-mt-subtype-attribute">MF_MT_SUBTYPE</a>
</td>
<td><b>MFAudioFormat_AAC</b></td>
</tr>
<tr>
<td>
<a href="/windows/desktop/medfound/mf-mt-aac-payload-type">MF_MT_AAC_PAYLOAD_TYPE</a>
</td>
<td>0 (raw AAC) or 1 (ADTS)</td>
</tr>
</table>

### -param ppMediaSink [out]

Receives a pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasink">IMFMediaSink</a> interface. The caller must release the interface.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The ADTS media sink converts Advanced Audio Coding (AAC) audio packets into an ADTS stream. The primary use for this media sink is to stream ADTS over a network. The output is not an audio file, but a stream of audio frames with ADTS headers.

The media sink can accept raw AAC frames (<a href="/windows/desktop/medfound/mf-mt-aac-payload-type">MF_MT_AAC_PAYLOAD_TYPE</a> = 0) or ADTS packets (MF_MT_AAC_PAYLOAD_TYPE = 1). If the input is raw AAC, the media sink inserts an ADTS header at the start of each audio frame. If the input is ADTS packets, the media sink passes the packets through to the byte stream, without modification.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
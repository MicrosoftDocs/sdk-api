---
UID: NN:mfspatialaudio.IMFSpatialAudioObjectBuffer
title: IMFSpatialAudioObjectBuffer (mfspatialaudio.h)
description: Represents a section of audio data with associated positional and rendering metadata. Spatial audio objects are stored in IMFSpatialAudioSample instances, and allow passing of spatial audio information between Media Foundation components.
helpviewer_keywords: ["IMFSpatialAudioObjectBuffer","IMFSpatialAudioObjectBuffer interface [Media Foundation]","IMFSpatialAudioObjectBuffer interface [Media Foundation]","described","mf.imfspatialaudioobjectbuffer","mfspatialaudio/IMFSpatialAudioObjectBuffer"]
old-location: mf\imfspatialaudioobjectbuffer.htm
tech.root: mf
ms.assetid: 61E9BC6A-2120-4874-9053-E1D232DF1CCA
ms.date: 12/05/2018
ms.keywords: IMFSpatialAudioObjectBuffer, IMFSpatialAudioObjectBuffer interface [Media Foundation], IMFSpatialAudioObjectBuffer interface [Media Foundation],described, mf.imfspatialaudioobjectbuffer, mfspatialaudio/IMFSpatialAudioObjectBuffer
req.header: mfspatialaudio.h
req.include-header: Mfobjects.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
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
req.lib: Mfobjects.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFSpatialAudioObjectBuffer
 - mfspatialaudio/IMFSpatialAudioObjectBuffer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfobjects.lib
 - mfobjects.dll
api_name:
 - IMFSpatialAudioObjectBuffer
---

# IMFSpatialAudioObjectBuffer interface


## -description

Represents a section of audio data with
associated positional and rendering metadata.  Spatial audio objects are stored in <a href="/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudiosample">IMFSpatialAudioSample</a> instances, and allow passing of 
spatial audio information between Media Foundation components.

## -inheritance

The <b>IMFSpatialAudioObjectBuffer</b> interface inherits from <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer">IMFMediaBuffer</a>. <b>IMFSpatialAudioObjectBuffer</b> also has these types of members:

## -remarks

To get the audio data contained in the spatial audio object, use the    <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock">IMFMediaBuffer::Lock</a> and <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock">IMFMediaBuffer::Unlock</a> methods.

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer">IMFMediaBuffer</a>

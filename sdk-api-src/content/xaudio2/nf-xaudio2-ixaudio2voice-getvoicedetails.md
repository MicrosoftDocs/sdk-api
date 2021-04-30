---
UID: NF:xaudio2.IXAudio2Voice.GetVoiceDetails
title: IXAudio2Voice::GetVoiceDetails (xaudio2.h)
description: Returns information about the creation flags, input channels, and sample rate of a voice.
helpviewer_keywords: ["GetVoiceDetails","GetVoiceDetails method [XAudio2 Audio Mixing APIs]","GetVoiceDetails method [XAudio2 Audio Mixing APIs]","IXAudio2Voice interface","IXAudio2Voice interface [XAudio2 Audio Mixing APIs]","GetVoiceDetails method","IXAudio2Voice.GetVoiceDetails","IXAudio2Voice::GetVoiceDetails","xaudio2.ixaudio2voice_interface_getvoicedetails","xaudio2/IXAudio2Voice::GetVoiceDetails"]
old-location: xaudio2\ixaudio2voice_interface_getvoicedetails.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2voice.IXAudio2Voice.GetVoiceDetails(XAUDIO2_VOICE_DETAILS@)
ms.date: 12/05/2018
ms.keywords: GetVoiceDetails, GetVoiceDetails method [XAudio2 Audio Mixing APIs], GetVoiceDetails method [XAudio2 Audio Mixing APIs],IXAudio2Voice interface, IXAudio2Voice interface [XAudio2 Audio Mixing APIs],GetVoiceDetails method, IXAudio2Voice.GetVoiceDetails, IXAudio2Voice::GetVoiceDetails, xaudio2.ixaudio2voice_interface_getvoicedetails, xaudio2/IXAudio2Voice::GetVoiceDetails
req.header: xaudio2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IXAudio2Voice::GetVoiceDetails
 - xaudio2/IXAudio2Voice::GetVoiceDetails
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xaudio2.h
api_name:
 - IXAudio2Voice.GetVoiceDetails
---

# IXAudio2Voice::GetVoiceDetails


## -description

Returns information about the creation flags, input channels, and sample rate of a voice.

## -parameters

### -param pVoiceDetails [in, out]

<a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_details">XAUDIO2_VOICE_DETAILS</a> structure containing information about the voice.

## -returns

This method does not return a value.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voice">IXAudio2Voice</a>
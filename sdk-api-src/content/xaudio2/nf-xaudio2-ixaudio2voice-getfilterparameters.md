---
UID: NF:xaudio2.IXAudio2Voice.GetFilterParameters
title: IXAudio2Voice::GetFilterParameters (xaudio2.h)
description: Gets the voice's filter parameters.
helpviewer_keywords: ["GetFilterParameters","GetFilterParameters method [XAudio2 Audio Mixing APIs]","GetFilterParameters method [XAudio2 Audio Mixing APIs]","IXAudio2Voice interface","IXAudio2Voice interface [XAudio2 Audio Mixing APIs]","GetFilterParameters method","IXAudio2Voice.GetFilterParameters","IXAudio2Voice::GetFilterParameters","xaudio2.ixaudio2voice_interface_getfilterparameters","xaudio2/IXAudio2Voice::GetFilterParameters"]
old-location: xaudio2\ixaudio2voice_interface_getfilterparameters.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2voice.IXAudio2Voice.GetFilterParameters(XAUDIO2_FILTER_PARAMETERS@)
ms.date: 12/05/2018
ms.keywords: GetFilterParameters, GetFilterParameters method [XAudio2 Audio Mixing APIs], GetFilterParameters method [XAudio2 Audio Mixing APIs],IXAudio2Voice interface, IXAudio2Voice interface [XAudio2 Audio Mixing APIs],GetFilterParameters method, IXAudio2Voice.GetFilterParameters, IXAudio2Voice::GetFilterParameters, xaudio2.ixaudio2voice_interface_getfilterparameters, xaudio2/IXAudio2Voice::GetFilterParameters
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
 - IXAudio2Voice::GetFilterParameters
 - xaudio2/IXAudio2Voice::GetFilterParameters
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - XAudio2.h
api_name:
 - IXAudio2Voice.GetFilterParameters
---

# IXAudio2Voice::GetFilterParameters


## -description

Gets the voice's filter parameters.

## -parameters

### -param pParameters [out]

Pointer to an <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters">XAUDIO2_FILTER_PARAMETERS</a> structure containing the filter information.

## -returns

This method does not return a value.

## -remarks

<b>GetFilterParameters</b> will fail if the voice was not created with the XAUDIO2_VOICE_USEFILTER flag.



<b>GetFilterParameters</b> always returns this voice's actual current filter parameters. However, these may not match the parameters set by the most recent <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters">IXAudio2Voice::SetFilterParameters</a> call: the actual parameters are only changed the next time the audio engine runs after the <b>IXAudio2Voice::SetFilterParameters</b> call (or after the corresponding <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges">IXAudio2::CommitChanges</a> call, if <b>IXAudio2Voice::SetFilterParameters</b> was called with a deferred operation ID).



<div class="alert"><b>Note</b>  <b>GetFilterParameters</b> is usable only on source and submix voices and has no effect on mastering voices.</div>
<div> </div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voice">IXAudio2Voice</a>
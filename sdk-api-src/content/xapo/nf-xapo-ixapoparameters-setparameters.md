---
UID: NF:xapo.IXAPOParameters.SetParameters
title: IXAPOParameters::SetParameters (xapo.h)
description: Sets effect-specific parameters.
helpviewer_keywords: ["IXAPOParameters interface [XAudio2 Audio Mixing APIs]","SetParameters method","IXAPOParameters.SetParameters","IXAPOParameters::SetParameters","SetParameters","SetParameters method [XAudio2 Audio Mixing APIs]","SetParameters method [XAudio2 Audio Mixing APIs]","IXAPOParameters interface","xapo/IXAPOParameters::SetParameters","xaudio2.ixapoparameters_interface_setparameters"]
old-location: xaudio2\ixapoparameters_interface_setparameters.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixapoparameters.IXAPOParameters.SetParameters(const void,UINT32)
ms.date: 12/05/2018
ms.keywords: IXAPOParameters interface [XAudio2 Audio Mixing APIs],SetParameters method, IXAPOParameters.SetParameters, IXAPOParameters::SetParameters, SetParameters, SetParameters method [XAudio2 Audio Mixing APIs], SetParameters method [XAudio2 Audio Mixing APIs],IXAPOParameters interface, xapo/IXAPOParameters::SetParameters, xaudio2.ixapoparameters_interface_setparameters
req.header: xapo.h
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
 - IXAPOParameters::SetParameters
 - xapo/IXAPOParameters::SetParameters
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - XAPO.h
api_name:
 - IXAPOParameters.SetParameters
---

# IXAPOParameters::SetParameters


## -description

Sets effect-specific parameters.

## -parameters

### -param pParameters

Effect-specific parameter block.

### -param ParameterByteSize

Size of pParameters, in bytes.

## -remarks

The data in <i>pParameters</i> is completely effect-specific and determined by the implementation of the <b>IXAPOParameters::SetParameters</b> function. The data passed to <b>SetParameters</b> can be used to set the state of the XAPO and control the behavior of the <a href="/windows/desktop/api/xapo/nf-xapo-ixapo-process">IXAPO::Process</a> function.



<b>SetParameters</b> can only be called on the real-time audio processing thread; no synchronization between <b>SetParameters</b> and the <a href="/windows/desktop/api/xapo/nf-xapo-ixapo-process">IXAPO::Process</a> method is necessary. However, the <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters">IXAudio2Voice::SetEffectParameters</a> method may be called from any thread as it adds in the required synchronization to deliver a copy (asynchronously) of the parameters to <b>SetParameters</b> on the real-time thread; no synchronization between <b>IXAudio2Voice::SetEffectParameters</b> and the <b>IXAPO::Process</b> method is necessary.



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/api/xapo/nn-xapo-ixapoparameters">IXAPOParameters</a>



<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters">IXAudio2Voice::SetEffectParameters</a>
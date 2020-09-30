---
UID: NF:xapo.IXAPOParameters.GetParameters
title: IXAPOParameters::GetParameters (xapo.h)
description: Gets the current values for any effect-specific parameters.
helpviewer_keywords: ["GetParameters","GetParameters method [XAudio2 Audio Mixing APIs]","GetParameters method [XAudio2 Audio Mixing APIs]","IXAPOParameters interface","IXAPOParameters interface [XAudio2 Audio Mixing APIs]","GetParameters method","IXAPOParameters.GetParameters","IXAPOParameters::GetParameters","xapo/IXAPOParameters::GetParameters","xaudio2.ixapoparameters_interface_getparameters"]
old-location: xaudio2\ixapoparameters_interface_getparameters.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixapoparameters.IXAPOParameters.GetParameters(void@,UINT32)
ms.date: 12/05/2018
ms.keywords: GetParameters, GetParameters method [XAudio2 Audio Mixing APIs], GetParameters method [XAudio2 Audio Mixing APIs],IXAPOParameters interface, IXAPOParameters interface [XAudio2 Audio Mixing APIs],GetParameters method, IXAPOParameters.GetParameters, IXAPOParameters::GetParameters, xapo/IXAPOParameters::GetParameters, xaudio2.ixapoparameters_interface_getparameters
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
 - IXAPOParameters::GetParameters
 - xapo/IXAPOParameters::GetParameters
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
 - IXAPOParameters.GetParameters
---

# IXAPOParameters::GetParameters


## -description

Gets the current values for any effect-specific parameters.

## -parameters

### -param pParameters [in, out]

Receives an effect-specific parameter block.

### -param ParameterByteSize [in]

Size of pParameters, in bytes.

## -remarks

The data in <i>pParameters</i> is completely effect-specific and determined by the implementation of the <b>IXAPOParameters::GetParameters</b> function. The data returned in <i>pParameters</i> can be used to provide information about the current state of the XAPO.



Unlike SetParameters, XAudio2 does not call this method on the realtime audio processing thread. Thus, the XAPO must protect variables shared with <a href="/windows/desktop/api/xapo/nf-xapo-ixapoparameters-setparameters">IXAPOParameters::SetParameters</a> or <a href="/windows/desktop/api/xapo/nf-xapo-ixapo-process">IXAPO::Process</a> using appropriate synchronization. The <a href="/windows/desktop/api/xapobase/nl-xapobase-cxapoparametersbase">CXAPOParametersBase</a> class is an implementation of <a href="/windows/desktop/api/xapo/nn-xapo-ixapoparameters">IXAPOParameters</a> and its implementation of <b>GetParameters</b> efficiently handles this synchronization for the user.



XAudio2 calls this method from the <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-geteffectparameters">IXAudio2Voice::GetEffectParameters</a> method.



This method may block and should never be called from the realtime audio processing thread instead get the current parameters from <a href="/windows/desktop/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess">CXAPOParametersBase::BeginProcess</a>.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/api/xapo/nn-xapo-ixapoparameters">IXAPOParameters</a>



<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-geteffectparameters">IXAudio2Voice::GetEffectParameters</a>
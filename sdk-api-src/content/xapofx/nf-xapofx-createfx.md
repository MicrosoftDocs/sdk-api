---
UID: NF:xapofx.CreateFX
title: CreateFX function (xapofx.h)
description: Creates an instance of the requested XAPOFX effect.
helpviewer_keywords: ["CreateFX","CreateFX function [XAudio2 Audio Mixing APIs]","xapofx/CreateFX","xaudio2.createfx"]
old-location: xaudio2\createfx.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.xapofx.CreateFX(CLSID,IUnknown,void,UINT32)
ms.date: 12/05/2018
ms.keywords: CreateFX, CreateFX function [XAudio2 Audio Mixing APIs], xapofx/CreateFX, xaudio2.createfx
req.header: xapofx.h
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
req.lib: XAudio.lib
req.dll: Windows.Media.Audio.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateFX
 - xapofx/CreateFX
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Windows.Media.Audio.dll
api_name:
 - CreateFX
---

# CreateFX function


## -description

Creates an instance of the requested <a href="/windows/desktop/xaudio2/xapofx-overview">XAPOFX</a> effect.

## -parameters

### -param clsid

ID of the effect to create. Use the <b>__uuidof</b> on the effect class name to get the CLSID for an effect. For example, <b>__uuidof</b>(FXReverb) would provide the CLSID for the FXReverb effect. For a list of effects provided by XAPOFX, see <a href="/windows/desktop/xaudio2/xapofx-overview">XAPOFX Overview</a>. For an example of retrieving the CLSID for an effect, see <a href="/windows/desktop/xaudio2/how-to--use-xapofx-in-xaudio2">How to: Use XAPOFX in XAudio2</a>.

### -param pEffect

Receives a pointer to the created XAPO instance. If <b>CreateFX</b> fails, <i>pEffect </i> is untouched.

### -param pInitData [optional]

Effect-specific initialization parameters. This is <b>NULL</b> if <i>InitDataByteSize</i> is zero.

### -param InitDataByteSize [optional]

Size of <i>pInitData</i> in bytes. This is zero if <i>pInitData</i> is <b>NULL</b>.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The created XAPO will have a reference count of 1. Client code must call <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-release">IUnknown::Release</a> after passing the XAPO to XAudio2 to allow XAudio2 to dispose of the XAPO when it is no longer needed. Use <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice"> IXAudio2::CreateSourceVoice</a> or <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain">IXAudio2Voice::SetEffectChain</a> to pass an XAPO to XAudio2.



<div class="alert"><b>Note</b>  The DirectX SDK version of this function doesn't have the <i>pInitData</i> or <i>InitDataByteSize</i> parameters as it only takes the first 2 parameters. To set initial parameters for the <a href="/windows/desktop/xaudio2/xapofx-overview">XAPOFX</a> effect that is  created with the DirectX SDK version of this function, you must bind that effect to a voice and use <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters">IXAudio2Voice::SetEffectParameters</a>.
For info about how to do this, see <a href="/windows/desktop/xaudio2/how-to--use-xapofx-in-xaudio2">How to: Use XAPOFX in XAudio2</a>.</div>
<div> </div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); 
            Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/functions">Functions</a>
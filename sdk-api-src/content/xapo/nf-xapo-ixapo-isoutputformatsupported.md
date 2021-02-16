---
UID: NF:xapo.IXAPO.IsOutputFormatSupported
title: IXAPO::IsOutputFormatSupported (xapo.h)
description: Queries if a specific output format is supported for a given input format.
helpviewer_keywords: ["IXAPO interface [XAudio2 Audio Mixing APIs]","IsOutputFormatSupported method","IXAPO.IsOutputFormatSupported","IXAPO::IsOutputFormatSupported","IsOutputFormatSupported","IsOutputFormatSupported method [XAudio2 Audio Mixing APIs]","IsOutputFormatSupported method [XAudio2 Audio Mixing APIs]","IXAPO interface","xapo/IXAPO::IsOutputFormatSupported","xaudio2.ixapo_interface_isoutputformatsupported"]
old-location: xaudio2\ixapo_interface_isoutputformatsupported.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixapo.IXAPO.IsOutputFormatSupported(const WAVEFORMATEX,const WAVEFORMATEX,WAVEFORMATEX@)
ms.date: 12/05/2018
ms.keywords: IXAPO interface [XAudio2 Audio Mixing APIs],IsOutputFormatSupported method, IXAPO.IsOutputFormatSupported, IXAPO::IsOutputFormatSupported, IsOutputFormatSupported, IsOutputFormatSupported method [XAudio2 Audio Mixing APIs], IsOutputFormatSupported method [XAudio2 Audio Mixing APIs],IXAPO interface, xapo/IXAPO::IsOutputFormatSupported, xaudio2.ixapo_interface_isoutputformatsupported
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
 - IXAPO::IsOutputFormatSupported
 - xapo/IXAPO::IsOutputFormatSupported
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
 - IXAPO.IsOutputFormatSupported
---

# IXAPO::IsOutputFormatSupported


## -description

Queries if a specific output format is supported for a given input format.

## -parameters

### -param pInputFormat [in]

Input format.

### -param pRequestedOutputFormat [in]

Output format to check for being supported.

### -param ppSupportedOutputFormat [out]

If not NULL and the output format is not supported for the given input format, <i>ppSupportedOutputFormat</i> returns a pointer to the closest output format that is supported. Use <a href="/windows/desktop/api/xapo/nf-xapo-xapofree">XAPOFree</a> to free the returned structure.

## -returns

Returns S_OK if the format pair is supported. Returns XAPO_E_FORMAT_UNSUPPORTED if the format pair is not supported.

## -remarks

The <a href="/windows/desktop/api/xapo/nf-xapo-ixapo-isinputformatsupported">IXAPO::IsInputFormatSupported</a> and <b>IsOutputFormatSupported</b> methods allow an XAPO to indicate which audio formats it is capable of processing. If a requested format is not supported, the XAPO should return the closest format that it does support. The closest format should be determined based on frame rate, bit depth, and channel count, in that order of importance. The behavior of <b>IsOutputFormatSupported</b> is allowed to change, based on the internal state of the XAPO, but its behavior should remain constant between calls to the <a href="/windows/desktop/api/xapo/nf-xapo-ixapo-lockforprocess">IXAPO::LockForProcess</a> and <a href="/windows/desktop/api/xapo/nf-xapo-ixapo-unlockforprocess">IXAPO::UnlockForProcess</a> methods.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/api/xapo/nn-xapo-ixapo">IXAPO</a>
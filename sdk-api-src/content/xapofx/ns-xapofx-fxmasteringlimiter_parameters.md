---
UID: NS:xapofx.FXMASTERINGLIMITER_PARAMETERS
title: FXMASTERINGLIMITER_PARAMETERS (xapofx.h)
description: Parameters for use with the FXMasteringLimiter XAPO.
helpviewer_keywords: ["FXMASTERINGLIMITER_PARAMETERS","FXMASTERINGLIMITER_PARAMETERS structure [XAudio2 Audio Mixing APIs]","xapofx/FXMASTERINGLIMITER_PARAMETERS","xaudio2.fxmasteringlimiter_parameters"]
old-location: xaudio2\fxmasteringlimiter_parameters.htm
tech.root: xaudio2
ms.assetid: T:Microsoft.directx_sdk.xapofx.FXMASTERINGLIMITER_PARAMETERS
ms.date: 12/05/2018
ms.keywords: FXMASTERINGLIMITER_PARAMETERS, FXMASTERINGLIMITER_PARAMETERS structure [XAudio2 Audio Mixing APIs], xapofx/FXMASTERINGLIMITER_PARAMETERS, xaudio2.fxmasteringlimiter_parameters
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FXMASTERINGLIMITER_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FXMASTERINGLIMITER_PARAMETERS
 - xapofx/FXMASTERINGLIMITER_PARAMETERS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - xapofx.h
api_name:
 - FXMASTERINGLIMITER_PARAMETERS
---

# FXMASTERINGLIMITER_PARAMETERS structure


## -description

Parameters for use with the <a href="/windows/desktop/xaudio2/xapofx-overview">FXMasteringLimiter  XAPO</a>.

## -struct-fields

### -field Release

Speed, in milliseconds, at which the limiter stops affecting audio after the audio drops below the limiter's threshold, which is specified by the <b>Loudness</b> member. This value must be between <a href="/windows/desktop/xaudio2/fxmasteringlimit-constants">FXMASTERINGLIMITER_MIN_RELEASE (1)</a> and <a href="/windows/desktop/xaudio2/fxmasteringlimit-constants">FXMASTERINGLIMITER_MAX_RELEASE (20)</a> and defaults to <a href="/windows/desktop/xaudio2/fxmasteringlimit-constants">FXMASTERINGLIMITER_DEFAULT_RELEASE (6)</a>.

### -field Loudness

Loudness metric threshold of the limiter. This value must be between <a href="/windows/desktop/xaudio2/fxmasteringlimit-constants">FXMASTERINGLIMITER_MIN_LOUDNESS (1)</a> and <a href="/windows/desktop/xaudio2/fxmasteringlimit-constants">FXMASTERINGLIMITER_MAX_LOUDNESS (1800)</a> and defaults to <a href="/windows/desktop/xaudio2/fxmasteringlimit-constants">FXMASTERINGLIMITER_DEFAULT_LOUDNESS (1000)</a>.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); 
            Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/structures">Structures</a>
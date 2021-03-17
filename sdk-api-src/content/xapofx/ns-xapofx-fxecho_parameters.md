---
UID: NS:xapofx.FXECHO_PARAMETERS
title: FXECHO_PARAMETERS (xapofx.h)
description: Parameters for use with the FXECHO XAPOFX.
helpviewer_keywords: ["FXECHO_PARAMETERS","FXECHO_PARAMETERS structure [XAudio2 Audio Mixing APIs]","xapofx/FXECHO_PARAMETERS","xaudio2.fxecho_parameters"]
old-location: xaudio2\fxecho_parameters.htm
tech.root: xaudio2
ms.assetid: T:Microsoft.directx_sdk.xapofx.FXECHO_PARAMETERS
ms.date: 12/05/2018
ms.keywords: FXECHO_PARAMETERS, FXECHO_PARAMETERS structure [XAudio2 Audio Mixing APIs], xapofx/FXECHO_PARAMETERS, xaudio2.fxecho_parameters
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
req.typenames: FXECHO_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FXECHO_PARAMETERS
 - xapofx/FXECHO_PARAMETERS
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
 - FXECHO_PARAMETERS
---

# FXECHO_PARAMETERS structure


## -description

Parameters for use with the <a href="/windows/desktop/xaudio2/xapofx-overview">FXECHO XAPOFX</a>.

## -struct-fields

### -field WetDryMix

Ratio of wet (processed) signal to dry (original) signal.

### -field Feedback

Amount of output to feed back into input.

### -field Delay

Delay to all channels in milliseconds. This value must be between <b>FXECHO_MIN_DELAY</b> and <a href="/windows/desktop/api/xapofx/ns-xapofx-fxecho_initdata">FXECHO_INITDATA</a>.<b>MaxDelay</b>.

## -remarks

Echo only supports FLOAT32 audio formats.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/structures">Structures</a>
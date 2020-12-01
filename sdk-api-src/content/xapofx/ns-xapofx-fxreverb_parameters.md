---
UID: NS:xapofx.FXREVERB_PARAMETERS
title: FXREVERB_PARAMETERS (xapofx.h)
description: Parameters for use with the FXReverb XAPO.
helpviewer_keywords: ["FXREVERB_PARAMETERS","FXREVERB_PARAMETERS structure [XAudio2 Audio Mixing APIs]","xapofx/FXREVERB_PARAMETERS","xaudio2.fxreverb_parameters"]
old-location: xaudio2\fxreverb_parameters.htm
tech.root: xaudio2
ms.assetid: T:Microsoft.directx_sdk.xapofx.FXREVERB_PARAMETERS
ms.date: 12/05/2018
ms.keywords: FXREVERB_PARAMETERS, FXREVERB_PARAMETERS structure [XAudio2 Audio Mixing APIs], xapofx/FXREVERB_PARAMETERS, xaudio2.fxreverb_parameters
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
req.typenames: FXREVERB_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FXREVERB_PARAMETERS
 - xapofx/FXREVERB_PARAMETERS
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
 - FXREVERB_PARAMETERS
---

# FXREVERB_PARAMETERS structure


## -description

Parameters for use with the FXReverb XAPO.

## -struct-fields

### -field Diffusion

Controls the character of the individual wall reflections. Set to minimum value to simulate a hard flat surface and to maximum value to simulate a diffuse surface.Value must be between FXREVERB_MIN_DIFFUSION and FXREVERB_MAX_DIFFUSION.

### -field RoomSize

Size of the room. Value must be between FXREVERB_MIN_ROOMSIZE and FXREVERB_MAX_ROOMSIZE. Note that physical meaning of RoomSize is subjective and not tied to any particular units. A smaller value will result in reflections reaching the listener more quickly while reflections will take longer with larger values for RoomSize.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/structures">Structures</a>
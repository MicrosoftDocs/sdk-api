---
UID: NS:hrtfapoapi.HrtfApoInit
title: HrtfApoInit (hrtfapoapi.h)
description: Specifies parameters used to initialize HRTF spatial audio.
helpviewer_keywords: ["HrtfApoInit","HrtfApoInit structure [XAudio2 Audio Mixing APIs]","PHrtfApoInit","PHrtfApoInit structure pointer [XAudio2 Audio Mixing APIs]","hrtfapoapi/HrtfApoInit","hrtfapoapi/PHrtfApoInit","xaudio2.hrtfapoinit"]
old-location: xaudio2\hrtfapoinit.htm
tech.root: xaudio2
ms.assetid: 686A2203-A991-427F-9D41-F3C679070127
ms.date: 12/05/2018
ms.keywords: HrtfApoInit, HrtfApoInit structure [XAudio2 Audio Mixing APIs], PHrtfApoInit, PHrtfApoInit structure pointer [XAudio2 Audio Mixing APIs], hrtfapoapi/HrtfApoInit, hrtfapoapi/PHrtfApoInit, xaudio2.hrtfapoinit
req.header: hrtfapoapi.h
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
req.typenames: HrtfApoInit
req.redist: 
ms.custom: 19H1
f1_keywords:
 - HrtfApoInit
 - hrtfapoapi/HrtfApoInit
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - HrtfApoApi.h
api_name:
 - HrtfApoInit
---

# HrtfApoInit structure


## -description

Specifies parameters used to initialize HRTF spatial audio.

## -struct-fields

### -field distanceDecay

The decay type. If you pass in nullptr, the default value is used. The default is natural decay.

### -field directivity

The directivity type. If you pass in nullptr, the default value is used. The default directivity is omni-directional.

## -see-also

<a href="/windows/desktop/api/hrtfapoapi/nf-hrtfapoapi-createhrtfapo">CreateHrtfApo</a>



<a href="/windows/desktop/xaudio2/structures">Structures</a>
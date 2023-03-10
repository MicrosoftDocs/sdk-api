---
UID: NS:hrtfapoapi.HrtfDirectivityCardioid
title: HrtfDirectivityCardioid (hrtfapoapi.h)
description: Describes a cardioid directivity pattern.
helpviewer_keywords: ["HrtfDirectivityCardioid","HrtfDirectivityCardioid structure [XAudio2 Audio Mixing APIs]","PHrtfDirectivityCardioid","PHrtfDirectivityCardioid structure pointer [XAudio2 Audio Mixing APIs]","hrtfapoapi/HrtfDirectivityCardioid","hrtfapoapi/PHrtfDirectivityCardioid","xaudio2.hrtfdirectivitycardioid"]
old-location: xaudio2\hrtfdirectivitycardioid.htm
tech.root: xaudio2
ms.assetid: 0705BB4C-01FE-434A-889B-F0D24D06DEF3
ms.date: 12/05/2018
ms.keywords: HrtfDirectivityCardioid, HrtfDirectivityCardioid structure [XAudio2 Audio Mixing APIs], PHrtfDirectivityCardioid, PHrtfDirectivityCardioid structure pointer [XAudio2 Audio Mixing APIs], hrtfapoapi/HrtfDirectivityCardioid, hrtfapoapi/PHrtfDirectivityCardioid, xaudio2.hrtfdirectivitycardioid
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
req.typenames: HrtfDirectivityCardioid
req.redist: 
ms.custom: 19H1
f1_keywords:
 - HrtfDirectivityCardioid
 - hrtfapoapi/HrtfDirectivityCardioid
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
 - HrtfDirectivityCardioid
---

# HrtfDirectivityCardioid structure


## -description

Describes a cardioid directivity pattern.

## -struct-fields

### -field directivity

Descriptor for the cardioid pattern. The type parameter must be set to HrtfDirectivityType.Cardioid.

### -field order

Controls the shape of the cardioid. The higher order the shape, the narrower it is. Must be greater than 0 and less than or equal to 32.

## -see-also

<a href="/windows/desktop/api/hrtfapoapi/ns-hrtfapoapi-hrtfdirectivity">HrtfDirectivity</a>



<a href="/windows/desktop/api/hrtfapoapi/ns-hrtfapoapi-hrtfdirectivitycone">HrtfDirectivityCone</a>



<a href="/windows/desktop/xaudio2/structures">Structures</a>
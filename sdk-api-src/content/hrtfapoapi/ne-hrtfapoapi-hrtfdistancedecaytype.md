---
UID: NE:hrtfapoapi.HrtfDistanceDecayType
title: HrtfDistanceDecayType (hrtfapoapi.h)
description: Indicates a distance-based decay type applied to a sound.
helpviewer_keywords: ["CustomDecay","HrtfDistanceDecayType","HrtfDistanceDecayType enumeration [XAudio2 Audio Mixing APIs]","NaturalDecay","hrtfapoapi/CustomDecay","hrtfapoapi/HrtfDistanceDecayType","hrtfapoapi/NaturalDecay","xaudio2.hrtfdistancedecaytype"]
old-location: xaudio2\hrtfdistancedecaytype.htm
tech.root: xaudio2
ms.assetid: 72421F09-6DB6-4195-AE44-0D3AD17F50B3
ms.date: 12/05/2018
ms.keywords: CustomDecay, HrtfDistanceDecayType, HrtfDistanceDecayType enumeration [XAudio2 Audio Mixing APIs], NaturalDecay, hrtfapoapi/CustomDecay, hrtfapoapi/HrtfDistanceDecayType, hrtfapoapi/NaturalDecay, xaudio2.hrtfdistancedecaytype
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
req.typenames: HrtfDistanceDecayType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - HrtfDistanceDecayType
 - hrtfapoapi/HrtfDistanceDecayType
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
 - HrtfDistanceDecayType
---

# HrtfDistanceDecayType enumeration


## -description

Indicates a distance-based decay type applied to a sound.

## -enum-fields

### -field NaturalDecay:0

Simulates natural decay with distance, as constrained by minimum and maximum gain distance limits. Drops to silence at rolloff distance.

### -field CustomDecay

Used to set up a custom gain curve, within the maximum and minimum gain limit.

## -see-also

<a href="/windows/desktop/xaudio2/enumerations">Enumerations</a>



<a href="/windows/desktop/api/hrtfapoapi/ns-hrtfapoapi-hrtfdistancedecay">HrtfDistanceDecay</a>

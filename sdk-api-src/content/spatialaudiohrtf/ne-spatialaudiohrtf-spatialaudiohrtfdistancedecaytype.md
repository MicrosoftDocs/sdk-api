---
UID: NE:spatialaudiohrtf.SpatialAudioHrtfDistanceDecayType
title: SpatialAudioHrtfDistanceDecayType (spatialaudiohrtf.h)

description: Specifies the type of decay applied over distance from the position of an ISpatialAudioObjectForHrtf to the position of the listener.
old-location: coreaudio\spatialaudiohrtfdistancedecaytype.htm
tech.root: CoreAudio
ms.assetid: EF4ACEB1-E802-4337-AA76-467BCB90D7C6

ms.date: 12/05/2018
ms.keywords: SpatialAudioHrtfDistanceDecayType, SpatialAudioHrtfDistanceDecayType enumeration [Core Audio], SpatialAudioHrtfDistanceDecay_CustomDecay, SpatialAudioHrtfDistanceDecay_NaturalDecay, coreaudio.spatialaudiohrtfdistancedecaytype, spatialaudiohrtf/ SpatialAudioHrtfDistanceDecay_NaturalDecay, spatialaudiohrtf/SpatialAudioHrtfDistanceDecayType, spatialaudiohrtf/SpatialAudioHrtfDistanceDecay_CustomDecay
ms.topic: enum
f1_keywords: 
 - "spatialaudiohrtf/SpatialAudioHrtfDistanceDecayType"
dev_langs:
 - c++
req.header: spatialaudiohrtf.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - spatialaudiohrtf.h
api_name:
 - SpatialAudioHrtfDistanceDecayType
targetos: Windows
req.typenames: SpatialAudioHrtfDistanceDecayType
req.redist: 
ms.custom: 19H1
---

# SpatialAudioHrtfDistanceDecayType enumeration


## -description


Specifies the type of decay applied over distance from the position of an <a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf">ISpatialAudioObjectForHrtf</a> to the position of the listener.


## -enum-fields




### -field SpatialAudioHrtfDistanceDecay_NaturalDecay

A natural decay  over distance, as constrained by minimum and maximum gain distance limits. The output drops to silent at the distance specified by <a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfdistancedecay">SpatialAudioHrtfDistanceDecay.CutoffDistance</a>.


### -field SpatialAudioHrtfDistanceDecay_CustomDecay

A custom gain curve, within the maximum and minimum gain limit.


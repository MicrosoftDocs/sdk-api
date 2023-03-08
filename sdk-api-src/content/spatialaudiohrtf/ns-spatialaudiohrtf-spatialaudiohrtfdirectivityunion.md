---
UID: NS:spatialaudiohrtf.SpatialAudioHrtfDirectivityUnion
title: SpatialAudioHrtfDirectivityUnion (spatialaudiohrtf.h)
description: Defines a spatial audio directivity model for an ISpatialAudioObjectForHrtf.
helpviewer_keywords: ["SpatialAudioHrtfDirectivityUnion","SpatialAudioHrtfDirectivityUnion union [Core Audio]","coreaudio.spatialaudiohrtfdirectivityunion","spatialaudiohrtf/SpatialAudioHrtfDirectivityUnion"]
old-location: coreaudio\spatialaudiohrtfdirectivityunion.htm
tech.root: CoreAudio
ms.assetid: BBBE4B0B-59C2-44E0-9BB4-B10CE5CE12E3
ms.date: 12/05/2018
ms.keywords: SpatialAudioHrtfDirectivityUnion, SpatialAudioHrtfDirectivityUnion union [Core Audio], coreaudio.spatialaudiohrtfdirectivityunion, spatialaudiohrtf/SpatialAudioHrtfDirectivityUnion
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
targetos: Windows
req.typenames: SpatialAudioHrtfDirectivityUnion
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SpatialAudioHrtfDirectivityUnion
 - spatialaudiohrtf/SpatialAudioHrtfDirectivityUnion
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - spatialaudiohrtf.h
api_name:
 - SpatialAudioHrtfDirectivityUnion
---

# SpatialAudioHrtfDirectivityUnion structure


## -description

Defines a spatial audio directivity model for an <a href="/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf">ISpatialAudioObjectForHrtf</a>.

## -struct-fields

### -field Cone

 A cone-shaped directivity model

### -field Cardioid

### -field Omni

And omni-direction directivity model that can be interpolated linearly with one of the other directivity models.


#### - Cardioid

 A cardioid-shaped directivity model
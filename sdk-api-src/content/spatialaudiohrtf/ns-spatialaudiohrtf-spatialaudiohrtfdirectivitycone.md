---
UID: NS:spatialaudiohrtf.SpatialAudioHrtfDirectivityCone
title: SpatialAudioHrtfDirectivityCone (spatialaudiohrtf.h)
description: Represents a cone-shaped directivity model for an ISpatialAudioObjectForHrtf.
helpviewer_keywords: ["PSpatialAudioHrtfDirectivityCone","PSpatialAudioHrtfDirectivityCone structure pointer [Core Audio]","SpatialAudioHrtfDirectivityCone","SpatialAudioHrtfDirectivityCone structure [Core Audio]","coreaudio.spatialaudiohrtfdirectivitycone","spatialaudiohrtf/PSpatialAudioHrtfDirectivityCone","spatialaudiohrtf/SpatialAudioHrtfDirectivityCone"]
old-location: coreaudio\spatialaudiohrtfdirectivitycone.htm
tech.root: CoreAudio
ms.assetid: C34F26C2-4979-4C06-8EAC-64547745238F
ms.date: 12/05/2018
ms.keywords: PSpatialAudioHrtfDirectivityCone, PSpatialAudioHrtfDirectivityCone structure pointer [Core Audio], SpatialAudioHrtfDirectivityCone, SpatialAudioHrtfDirectivityCone structure [Core Audio], coreaudio.spatialaudiohrtfdirectivitycone, spatialaudiohrtf/PSpatialAudioHrtfDirectivityCone, spatialaudiohrtf/SpatialAudioHrtfDirectivityCone
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
req.typenames: SpatialAudioHrtfDirectivityCone
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SpatialAudioHrtfDirectivityCone
 - spatialaudiohrtf/SpatialAudioHrtfDirectivityCone
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
 - SpatialAudioHrtfDirectivityCone
---

# SpatialAudioHrtfDirectivityCone structure


## -description

Represents a cone-shaped directivity model for an <a href="/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf">ISpatialAudioObjectForHrtf</a>.

## -struct-fields

### -field directivity

A structure that expresses the direction in which sound is emitted by an <a href="/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf">ISpatialAudioObjectForHrtf</a>.

### -field InnerAngle

The inner angle of the cone.

### -field OuterAngle

The outer angle of the cone.
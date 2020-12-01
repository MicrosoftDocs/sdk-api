---
UID: NS:spatialaudiohrtf.SpatialAudioHrtfDirectivity
title: SpatialAudioHrtfDirectivity (spatialaudiohrtf.h)
description: Represents an omnidirectional model for an ISpatialAudioObjectForHrtf. The omnidirectional emission is interpolated linearly with the directivity model specified in the Type field based on the value of the Scaling field.
helpviewer_keywords: ["PSpatialAudioHrtfDirectivity","PSpatialAudioHrtfDirectivity structure pointer [Core Audio]","SpatialAudioHrtfDirectivity","SpatialAudioHrtfDirectivity structure [Core Audio]","coreaudio.spatialaudiohrtfdirectivity","spatialaudiohrtf/PSpatialAudioHrtfDirectivity","spatialaudiohrtf/SpatialAudioHrtfDirectivity"]
old-location: coreaudio\spatialaudiohrtfdirectivity.htm
tech.root: CoreAudio
ms.assetid: A3D149E0-F2C1-47C7-8858-35C5F51C7F75
ms.date: 12/05/2018
ms.keywords: PSpatialAudioHrtfDirectivity, PSpatialAudioHrtfDirectivity structure pointer [Core Audio], SpatialAudioHrtfDirectivity, SpatialAudioHrtfDirectivity structure [Core Audio], coreaudio.spatialaudiohrtfdirectivity, spatialaudiohrtf/PSpatialAudioHrtfDirectivity, spatialaudiohrtf/SpatialAudioHrtfDirectivity
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
req.typenames: SpatialAudioHrtfDirectivity
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SpatialAudioHrtfDirectivity
 - spatialaudiohrtf/SpatialAudioHrtfDirectivity
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
 - SpatialAudioHrtfDirectivity
---

# SpatialAudioHrtfDirectivity structure


## -description

Represents an omnidirectional model for an <a href="/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf">ISpatialAudioObjectForHrtf</a>. The omnidirectional emission is interpolated linearly with the directivity model specified in the <b>Type</b> field based on the value of the <b>Scaling</b> field.

## -struct-fields

### -field Type

The type of shape in which sound is emitted by an <a href="/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf">ISpatialAudioObjectForHrtf</a>.

### -field Scaling

The amount of linear interpolation applied between omnidirectional sound and the directivity specified in the <b>Type</b> field. This is a normalized value between 0 and 1.0 where 0 is omnidirectional and 1.0 is full directivity using the specified type.
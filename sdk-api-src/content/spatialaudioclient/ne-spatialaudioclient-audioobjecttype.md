---
UID: NE:spatialaudioclient.AudioObjectType
title: AudioObjectType (spatialaudioclient.h)
description: Specifies the type of an ISpatialAudioObject.
helpviewer_keywords: ["AudioObjectType","AudioObjectType enumeration [Core Audio]","AudioObjectType_BackCenter","AudioObjectType_BackLeft","AudioObjectType_BackRight","AudioObjectType_BottomBackLeft","AudioObjectType_BottomBackRight","AudioObjectType_BottomFrontLeft","AudioObjectType_BottomFrontRight","AudioObjectType_Dynamic","AudioObjectType_FrontCenter","AudioObjectType_FrontLeft","AudioObjectType_FrontRight","AudioObjectType_LowFrequency","AudioObjectType_None","AudioObjectType_SideLeft","AudioObjectType_SideRight","AudioObjectType_TopBackLeft","AudioObjectType_TopBackRight","AudioObjectType_TopFrontLeft","AudioObjectType_TopFrontRight","coreaudio.audioobjecttype","spatialaudioclient/AudioObjectType","spatialaudioclient/AudioObjectType_BackCenter","spatialaudioclient/AudioObjectType_BackLeft","spatialaudioclient/AudioObjectType_BackRight","spatialaudioclient/AudioObjectType_BottomBackLeft","spatialaudioclient/AudioObjectType_BottomBackRight","spatialaudioclient/AudioObjectType_BottomFrontLeft","spatialaudioclient/AudioObjectType_BottomFrontRight","spatialaudioclient/AudioObjectType_Dynamic","spatialaudioclient/AudioObjectType_FrontCenter","spatialaudioclient/AudioObjectType_FrontLeft","spatialaudioclient/AudioObjectType_FrontRight","spatialaudioclient/AudioObjectType_LowFrequency","spatialaudioclient/AudioObjectType_None","spatialaudioclient/AudioObjectType_SideLeft","spatialaudioclient/AudioObjectType_SideRight","spatialaudioclient/AudioObjectType_TopBackLeft","spatialaudioclient/AudioObjectType_TopBackRight","spatialaudioclient/AudioObjectType_TopFrontLeft","spatialaudioclient/AudioObjectType_TopFrontRight"]
old-location: coreaudio\audioobjecttype.htm
tech.root: CoreAudio
ms.assetid: DFFE770F-41C0-4048-A38F-FB96353E9216
ms.date: 12/05/2018
ms.keywords: AudioObjectType, AudioObjectType enumeration [Core Audio], AudioObjectType_BackCenter, AudioObjectType_BackLeft, AudioObjectType_BackRight, AudioObjectType_BottomBackLeft, AudioObjectType_BottomBackRight, AudioObjectType_BottomFrontLeft, AudioObjectType_BottomFrontRight, AudioObjectType_Dynamic, AudioObjectType_FrontCenter, AudioObjectType_FrontLeft, AudioObjectType_FrontRight, AudioObjectType_LowFrequency, AudioObjectType_None, AudioObjectType_SideLeft, AudioObjectType_SideRight, AudioObjectType_TopBackLeft, AudioObjectType_TopBackRight, AudioObjectType_TopFrontLeft, AudioObjectType_TopFrontRight, coreaudio.audioobjecttype, spatialaudioclient/AudioObjectType, spatialaudioclient/AudioObjectType_BackCenter, spatialaudioclient/AudioObjectType_BackLeft, spatialaudioclient/AudioObjectType_BackRight, spatialaudioclient/AudioObjectType_BottomBackLeft, spatialaudioclient/AudioObjectType_BottomBackRight, spatialaudioclient/AudioObjectType_BottomFrontLeft, spatialaudioclient/AudioObjectType_BottomFrontRight, spatialaudioclient/AudioObjectType_Dynamic, spatialaudioclient/AudioObjectType_FrontCenter, spatialaudioclient/AudioObjectType_FrontLeft, spatialaudioclient/AudioObjectType_FrontRight, spatialaudioclient/AudioObjectType_LowFrequency, spatialaudioclient/AudioObjectType_None, spatialaudioclient/AudioObjectType_SideLeft, spatialaudioclient/AudioObjectType_SideRight, spatialaudioclient/AudioObjectType_TopBackLeft, spatialaudioclient/AudioObjectType_TopBackRight, spatialaudioclient/AudioObjectType_TopFrontLeft, spatialaudioclient/AudioObjectType_TopFrontRight
req.header: spatialaudioclient.h
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
req.typenames: AudioObjectType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AudioObjectType
 - spatialaudioclient/AudioObjectType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - spatialaudioclient.h
api_name:
 - AudioObjectType
---

# AudioObjectType enumeration


## -description

Specifies the type of an <a href="/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject">ISpatialAudioObject</a>. A spatial audio object can be dynamic, meaning that its spatial properties can change over time, or static, which means that its spatial properties are fixed. There are 17 audio channels to which a static spatial audio object can be assigned, each representing a real or virtualized speaker. The static channel values of the enumeration can be combined as a mask to assign a spatial audio object to multiple channels. All of the enumeration values except for <b>AudioObjectType_None</b> and <b>AudioObjectType_Dynamic</b> represent static channels.

## -enum-fields

### -field AudioObjectType_None:0

The spatial audio object is not spatialized.

### -field AudioObjectType_Dynamic

The spatial audio object is dynamic. It's spatial properties can be changed over time.

### -field AudioObjectType_FrontLeft

The spatial audio object is assigned the front left channel. The equivalent channel mask of DirectShow's <a href="/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)">WAVEFORMATEXTENSIBLE</a> enumeration is SPEAKER_FRONT_LEFT.

### -field AudioObjectType_FrontRight

The spatial audio object is assigned the front right channel. The equivalent channel mask of DirectShow's <a href="/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)">WAVEFORMATEXTENSIBLE</a> enumeration is SPEAKER_FRONT_RIGHT.

### -field AudioObjectType_FrontCenter

The spatial audio object is assigned the front center channel. The equivalent channel mask of DirectShow's <a href="/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)">WAVEFORMATEXTENSIBLE</a> enumeration is SPEAKER_FRONT_CENTER.

### -field AudioObjectType_LowFrequency

The spatial audio object is assigned the low frequency channel. Because this channel is not spatialized, it does not count toward the system resource limits for spatialized audio objects. The equivalent channel mask of DirectShow's <a href="/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)">WAVEFORMATEXTENSIBLE</a> enumeration is SPEAKER_LOW_FREQUENCY.

### -field AudioObjectType_SideLeft

The spatial audio object is assigned the side left channel. The equivalent channel mask of DirectShow's <a href="/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)">WAVEFORMATEXTENSIBLE</a> enumeration is SPEAKER_SIDE_LEFT.

### -field AudioObjectType_SideRight

The spatial audio object is assigned the side right channel. The equivalent channel mask of DirectShow's <a href="/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)">WAVEFORMATEXTENSIBLE</a> enumeration is SPEAKER_SIDE_RIGHT.

### -field AudioObjectType_BackLeft

The spatial audio object is assigned the back left channel. The equivalent channel mask of DirectShow's <a href="/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)">WAVEFORMATEXTENSIBLE</a> enumeration is SPEAKER_BACK_LEFT.

### -field AudioObjectType_BackRight

The spatial audio object is assigned the back right channel. The equivalent channel mask of DirectShow's <a href="/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)">WAVEFORMATEXTENSIBLE</a> enumeration is SPEAKER_BACK_RIGHT.

### -field AudioObjectType_TopFrontLeft

The spatial audio object is assigned the top front left channel. The equivalent channel mask of DirectShow's <a href="/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)">WAVEFORMATEXTENSIBLE</a> enumeration is SPEAKER_TOP_FRONT_LEFT.

### -field AudioObjectType_TopFrontRight

The spatial audio object is assigned the top front right channel. The equivalent channel mask of DirectShow's <a href="/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)">WAVEFORMATEXTENSIBLE</a> enumeration is SPEAKER_TOP_FRONT_RIGHT.

### -field AudioObjectType_TopBackLeft

The spatial audio object is assigned the top back left channel. The equivalent channel mask of DirectShow's <a href="/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)">WAVEFORMATEXTENSIBLE</a> enumeration is SPEAKER_TOP_BACK_LEFT.

### -field AudioObjectType_TopBackRight

The spatial audio object is assigned the top back right channel. The equivalent channel mask of DirectShow's <a href="/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)">WAVEFORMATEXTENSIBLE</a> enumeration is SPEAKER_TOP_BACK_RIGHT.

### -field AudioObjectType_BottomFrontLeft

The spatial audio object is assigned the bottom front left channel.

### -field AudioObjectType_BottomFrontRight

The spatial audio object is assigned the bottom front right channel.

### -field AudioObjectType_BottomBackLeft

The spatial audio object is assigned the bottom back left channel.

### -field AudioObjectType_BottomBackRight

The spatial audio object is assigned the bottom back right channel.

### -field AudioObjectType_BackCenter

The spatial audio object is assigned the back center channel.

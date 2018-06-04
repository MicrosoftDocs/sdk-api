---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# AudioObjectType enumeration


## -description


Specifies the type of an <a href="https://msdn.microsoft.com/EE83AF5F-4342-4CF2-81A7-1123F8DAFA6F">ISpatialAudioObject</a>. A spatial audio object can be dynamic, meaning that it's spatial properties can change over time, or static, which means that its spatial properties are fixed. There are 17 audio channels to which a static spatial audio object can be assigned, each representing a real or virtualized speaker. The static channel values of the enumeration can be combined as a mask to assign a spatial audio object to multiple channels. All of the enumeration values except for <b>AudioObjectType_None</b> and <b>AudioObjectType_Dynamic</b> represent static channels.


## -enum-fields




### -field AudioObjectType_None

The spatial audio object is not spatialized.


### -field AudioObjectType_Dynamic

The spatial audio object is dynamic. It's spatial properties can be changed over time.


### -field AudioObjectType_FrontLeft

The spatial audio object is assigned the front left channel. The equivalent channel mask of DirectShow's <a href="https://msdn.microsoft.com/library/windows/hardware/ff538802">WAVEFORMATEXTENSIBLE</a> enumeration is SPEAKER_FRONT_LEFT. 


### -field AudioObjectType_FrontRight

The spatial audio object is assigned the front right channel. The equivalent channel mask of DirectShow's <a href="https://msdn.microsoft.com/library/windows/hardware/ff538802">WAVEFORMATEXTENSIBLE</a> enumeration is SPEAKER_FRONT_RIGHT. 


### -field AudioObjectType_FrontCenter

The spatial audio object is assigned the front center channel. The equivalent channel mask of DirectShow's <a href="https://msdn.microsoft.com/library/windows/hardware/ff538802">WAVEFORMATEXTENSIBLE</a> enumeration is SPEAKER_FRONT_CENTER. 


### -field AudioObjectType_LowFrequency

The spatial audio object is assigned the low frequency channel. Because this channel is not spatialized, it does not count toward the system resource limits for spatialized audio objects. The equivalent channel mask of DirectShow's <a href="https://msdn.microsoft.com/library/windows/hardware/ff538802">WAVEFORMATEXTENSIBLE</a> enumeration is SPEAKER_LOW_FREQUENCY. 


### -field AudioObjectType_SideLeft

The spatial audio object is assigned the side left channel. The equivalent channel mask of DirectShow's <a href="https://msdn.microsoft.com/library/windows/hardware/ff538802">WAVEFORMATEXTENSIBLE</a> enumeration is SPEAKER_SIDE_LEFT. 


### -field AudioObjectType_SideRight

The spatial audio object is assigned the side right channel. The equivalent channel mask of DirectShow's <a href="https://msdn.microsoft.com/library/windows/hardware/ff538802">WAVEFORMATEXTENSIBLE</a> enumeration is SPEAKER_SIDE_RIGHT. 


### -field AudioObjectType_BackLeft

The spatial audio object is assigned the back left channel. The equivalent channel mask of DirectShow's <a href="https://msdn.microsoft.com/library/windows/hardware/ff538802">WAVEFORMATEXTENSIBLE</a> enumeration is SPEAKER_BACK_LEFT. 


### -field AudioObjectType_BackRight

The spatial audio object is assigned the back right channel. The equivalent channel mask of DirectShow's <a href="https://msdn.microsoft.com/library/windows/hardware/ff538802">WAVEFORMATEXTENSIBLE</a> enumeration is SPEAKER_BACK_RIGHT. 


### -field AudioObjectType_TopFrontLeft

The spatial audio object is assigned the top front left channel. The equivalent channel mask of DirectShow's <a href="https://msdn.microsoft.com/library/windows/hardware/ff538802">WAVEFORMATEXTENSIBLE</a> enumeration is SPEAKER_TOP_FRONT_LEFT. 


### -field AudioObjectType_TopFrontRight

The spatial audio object is assigned the top front right channel. The equivalent channel mask of DirectShow's <a href="https://msdn.microsoft.com/library/windows/hardware/ff538802">WAVEFORMATEXTENSIBLE</a> enumeration is SPEAKER_TOP_FRONT_RIGHT. 


### -field AudioObjectType_TopBackLeft

The spatial audio object is assigned the top back left channel. The equivalent channel mask of DirectShow's <a href="https://msdn.microsoft.com/library/windows/hardware/ff538802">WAVEFORMATEXTENSIBLE</a> enumeration is SPEAKER_TOP_BACK_LEFT. 


### -field AudioObjectType_TopBackRight

The spatial audio object is assigned the top back right channel. The equivalent channel mask of DirectShow's <a href="https://msdn.microsoft.com/library/windows/hardware/ff538802">WAVEFORMATEXTENSIBLE</a> enumeration is SPEAKER_TOP_BACK_RIGHT. 


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


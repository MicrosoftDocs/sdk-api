---
UID: NF:audioengineendpoint.IAudioEndpointOffloadStreamVolume.SetChannelVolumes
title: IAudioEndpointOffloadStreamVolume::SetChannelVolumes (audioengineendpoint.h)
author: windows-sdk-content
description: The SetChannelVolumes method sets the volume levels for the various audio channels in the offloaded stream.
old-location: coreaudio\iaudioendpointoffloadstreamvolume_setchannelvolumes.htm
tech.root: CoreAudio
ms.assetid: 80E736B5-AF8E-46B3-9CDF-753B045F60D9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAudioEndpointOffloadStreamVolume interface [Core Audio],SetChannelVolumes method, IAudioEndpointOffloadStreamVolume.SetChannelVolumes, IAudioEndpointOffloadStreamVolume::SetChannelVolumes, SetChannelVolumes, SetChannelVolumes method [Core Audio], SetChannelVolumes method [Core Audio],IAudioEndpointOffloadStreamVolume interface, audioengineendpoint/IAudioEndpointOffloadStreamVolume::SetChannelVolumes, coreaudio.iaudioendpointoffloadstreamvolume_setchannelvolumes
ms.topic: method
f1_keywords: 
 - "audioengineendpoint/IAudioEndpointOffloadStreamVolume.SetChannelVolumes"
dev_langs:
 - c++
req.header: audioengineendpoint.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - COM
api_location:
 - Audioengineendpoint.h
api_name:
 - IAudioEndpointOffloadStreamVolume.SetChannelVolumes
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAudioEndpointOffloadStreamVolume::SetChannelVolumes


## -description


The <b>SetChannelVolumes</b> method sets the volume levels for the various audio channels in the offloaded stream.


## -parameters




### -param u32ChannelCount [in]

Indicates the number of available audio channels in the offloaded stream.


### -param pf32Volumes [in]

A pointer to the volume levels for the various audio channels in the offloaded stream.


### -param u32CurveType

A value from the [AUDIO_CURVE_TYPE](https://docs.microsoft.com/windows-hardware/drivers/ddi/content/ksmedia/ne-ksmedia-audio_curve_type) enumeration specifying the curve to use when changing the channel volumes.


### -param pCurveDuration

A **LONGLONG** value specifying the curve duration in hundred nanosecond units.




## -returns



The <b>SetChannelVolumes</b> method returns <b>S_OK</b> to indicate that it has completed successfully. Otherwise it returns an appropriate error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/audioengineendpoint/nn-audioengineendpoint-iaudioendpointoffloadstreamvolume">IAudioEndpointOffloadStreamVolume</a>
 

 


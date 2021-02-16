---
UID: NF:audioengineendpoint.IAudioEndpointOffloadStreamVolume.SetChannelVolumes
title: IAudioEndpointOffloadStreamVolume::SetChannelVolumes (audioengineendpoint.h)
description: The SetChannelVolumes method sets the volume levels for the various audio channels in the offloaded stream.
helpviewer_keywords: ["IAudioEndpointOffloadStreamVolume interface [Core Audio]","SetChannelVolumes method","IAudioEndpointOffloadStreamVolume.SetChannelVolumes","IAudioEndpointOffloadStreamVolume::SetChannelVolumes","SetChannelVolumes","SetChannelVolumes method [Core Audio]","SetChannelVolumes method [Core Audio]","IAudioEndpointOffloadStreamVolume interface","audioengineendpoint/IAudioEndpointOffloadStreamVolume::SetChannelVolumes","coreaudio.iaudioendpointoffloadstreamvolume_setchannelvolumes"]
old-location: coreaudio\iaudioendpointoffloadstreamvolume_setchannelvolumes.htm
tech.root: CoreAudio
ms.assetid: 80E736B5-AF8E-46B3-9CDF-753B045F60D9
ms.date: 12/05/2018
ms.keywords: IAudioEndpointOffloadStreamVolume interface [Core Audio],SetChannelVolumes method, IAudioEndpointOffloadStreamVolume.SetChannelVolumes, IAudioEndpointOffloadStreamVolume::SetChannelVolumes, SetChannelVolumes, SetChannelVolumes method [Core Audio], SetChannelVolumes method [Core Audio],IAudioEndpointOffloadStreamVolume interface, audioengineendpoint/IAudioEndpointOffloadStreamVolume::SetChannelVolumes, coreaudio.iaudioendpointoffloadstreamvolume_setchannelvolumes
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAudioEndpointOffloadStreamVolume::SetChannelVolumes
 - audioengineendpoint/IAudioEndpointOffloadStreamVolume::SetChannelVolumes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audioengineendpoint.h
api_name:
 - IAudioEndpointOffloadStreamVolume.SetChannelVolumes
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

A value from the [AUDIO_CURVE_TYPE](/windows-hardware/drivers/ddi/content/ksmedia/ne-ksmedia-audio_curve_type) enumeration specifying the curve to use when changing the channel volumes.

### -param pCurveDuration

A **LONGLONG** value specifying the curve duration in hundred nanosecond units.

## -returns

The <b>SetChannelVolumes</b> method returns <b>S_OK</b> to indicate that it has completed successfully. Otherwise it returns an appropriate error code.

## -see-also

<a href="/windows/desktop/api/audioengineendpoint/nn-audioengineendpoint-iaudioendpointoffloadstreamvolume">IAudioEndpointOffloadStreamVolume</a>
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

TBD


### -param pCurveDuration

TBD




## -returns



The <b>SetChannelVolumes</b> method returns <b>S_OK</b> to indicate that it has completed successfully. Otherwise it returns an appropriate error code.




## -see-also




<a href="https://msdn.microsoft.com/73FD2289-8414-4A63-A518-634D6F2DF48D">IAudioEndpointOffloadStreamVolume</a>
 

 


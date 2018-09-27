---
UID: NF:audioengineendpoint.IAudioEndpointOffloadStreamVolume.GetChannelVolumes
title: IAudioEndpointOffloadStreamVolume::GetChannelVolumes
author: windows-sdk-content
description: The GetChannelVolumes method retrieves the volume levels for the various audio channels in the offloaded stream.
old-location: coreaudio\iaudioendpointoffloadstreamvolume_getchannelvolumes.htm
tech.root: CoreAudio
ms.assetid: B15CA88E-EDB3-4BB4-9B74-98BB1D0CE288
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: GetChannelVolumes, GetChannelVolumes method [Core Audio], GetChannelVolumes method [Core Audio],IAudioEndpointOffloadStreamVolume interface, IAudioEndpointOffloadStreamVolume interface [Core Audio],GetChannelVolumes method, IAudioEndpointOffloadStreamVolume.GetChannelVolumes, IAudioEndpointOffloadStreamVolume::GetChannelVolumes, audioengineendpoint/IAudioEndpointOffloadStreamVolume::GetChannelVolumes, coreaudio.iaudioendpointoffloadstreamvolume_getchannelvolumes
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IAudioEndpointOffloadStreamVolume.GetChannelVolumes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAudioEndpointOffloadStreamVolume::GetChannelVolumes


## -description


The <b>GetChannelVolumes</b> method retrieves the volume levels for the various audio channels in the offloaded stream.


## -parameters




### -param u32ChannelCount [in]

Indicates the numer of available audio channels in the offloaded stream.


### -param pf32Volumes [out]

A pointer to the volume levels for the various  audio channels in the offloaded stream.


## -returns



The <b>GetChannelVolumes</b> method returns <b>S_OK</b> to indicate that it has completed successfully. Otherwise it returns an appropriate error code.




## -see-also




<a href="https://msdn.microsoft.com/73FD2289-8414-4A63-A518-634D6F2DF48D">IAudioEndpointOffloadStreamVolume</a>
 

 


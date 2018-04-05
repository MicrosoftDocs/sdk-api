---
UID: NF:audioengineendpoint.IAudioEndpointOffloadStreamVolume.SetChannelVolumes
title: IAudioEndpointOffloadStreamVolume::SetChannelVolumes method
author: windows-driver-content
description: The SetChannelVolumes method sets the volume levels for the various audio channels in the offloaded stream.
old-location: coreaudio\iaudioendpointoffloadstreamvolume_setchannelvolumes.htm
old-project: CoreAudio
ms.assetid: 80E736B5-AF8E-46B3-9CDF-753B045F60D9
ms.author: windowsdriverdev
ms.date: 3/30/2018
ms.keywords: IAudioEndpointOffloadStreamVolume, IAudioEndpointOffloadStreamVolume interface [Core Audio], SetChannelVolumes method, IAudioEndpointOffloadStreamVolume::SetChannelVolumes, SetChannelVolumes method [Core Audio], SetChannelVolumes method [Core Audio], IAudioEndpointOffloadStreamVolume interface, SetChannelVolumes,IAudioEndpointOffloadStreamVolume.SetChannelVolumes, audioengineendpoint/IAudioEndpointOffloadStreamVolume::SetChannelVolumes, coreaudio.iaudioendpointoffloadstreamvolume_setchannelvolumes
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
req.typenames: AE_POSITION_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Audioengineendpoint.h
api_name:
-	IAudioEndpointOffloadStreamVolume.SetChannelVolumes
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAudioEndpointOffloadStreamVolume::SetChannelVolumes method


## -description


The <b>SetChannelVolumes</b> method sets the volume levels for the various audio channels in the offloaded stream.


## -parameters




### -param u32ChannelCount [in]

Indicates the number of available audio channels in the offloaded stream.


### -param pf32Volumes [in]

A pointer to the volume levels for the various audio channels in the offloaded stream.


### -param u32CurveType




### -param pCurveDuration






## -returns



The <b>SetChannelVolumes</b> method returns <b>S_OK</b> to indicate that it has completed successfully. Otherwise it returns an appropriate error code.




## -see-also




<a href="https://msdn.microsoft.com/73FD2289-8414-4A63-A518-634D6F2DF48D">IAudioEndpointOffloadStreamVolume</a>
 

 


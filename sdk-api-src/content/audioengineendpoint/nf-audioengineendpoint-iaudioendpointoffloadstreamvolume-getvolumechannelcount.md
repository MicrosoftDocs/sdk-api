---
UID: NF:audioengineendpoint.IAudioEndpointOffloadStreamVolume.GetVolumeChannelCount
title: IAudioEndpointOffloadStreamVolume::GetVolumeChannelCount
author: windows-sdk-content
description: The GetVolumeChannelCount method retrieves the number of available audio channels in the offloaded stream.
old-location: coreaudio\iaudioendpointoffloadstreamvolume_getvolumechannelcount.htm
old-project: CoreAudio
ms.assetid: 361E3B06-D543-4C86-BE0E-E3E0E2A51A27
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetVolumeChannelCount, GetVolumeChannelCount method [Core Audio], GetVolumeChannelCount method [Core Audio],IAudioEndpointOffloadStreamVolume interface, IAudioEndpointOffloadStreamVolume interface [Core Audio],GetVolumeChannelCount method, IAudioEndpointOffloadStreamVolume.GetVolumeChannelCount, IAudioEndpointOffloadStreamVolume::GetVolumeChannelCount, audioengineendpoint/IAudioEndpointOffloadStreamVolume::GetVolumeChannelCount, coreaudio.iaudioendpointoffloadstreamvolume_getvolumechannelcount
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AE_POSITION_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audioengineendpoint.h
api_name:
 - IAudioEndpointOffloadStreamVolume.GetVolumeChannelCount
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAudioEndpointOffloadStreamVolume::GetVolumeChannelCount


## -description


The <b>GetVolumeChannelCount</b> method retrieves the number of available  audio channels in the offloaded stream.


## -parameters




### -param pu32ChannelCount [out]

A pointer to the number of available audio channels in the offloaded stream.


## -returns



The <b>GetVolumeChannelCount</b> method returns <b>S_OK</b> to indicate that it has completed successfully. Otherwise it returns an appropriate error code.




## -see-also




<a href="https://msdn.microsoft.com/73FD2289-8414-4A63-A518-634D6F2DF48D">IAudioEndpointOffloadStreamVolume</a>
 

 


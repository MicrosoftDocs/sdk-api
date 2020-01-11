---
UID: NF:audioengineendpoint.IAudioEndpointOffloadStreamVolume.GetVolumeChannelCount
title: IAudioEndpointOffloadStreamVolume::GetVolumeChannelCount (audioengineendpoint.h)
description: The GetVolumeChannelCount method retrieves the number of available audio channels in the offloaded stream.
old-location: coreaudio\iaudioendpointoffloadstreamvolume_getvolumechannelcount.htm
tech.root: CoreAudio
ms.assetid: 361E3B06-D543-4C86-BE0E-E3E0E2A51A27
ms.date: 12/05/2018
ms.keywords: GetVolumeChannelCount, GetVolumeChannelCount method [Core Audio], GetVolumeChannelCount method [Core Audio],IAudioEndpointOffloadStreamVolume interface, IAudioEndpointOffloadStreamVolume interface [Core Audio],GetVolumeChannelCount method, IAudioEndpointOffloadStreamVolume.GetVolumeChannelCount, IAudioEndpointOffloadStreamVolume::GetVolumeChannelCount, audioengineendpoint/IAudioEndpointOffloadStreamVolume::GetVolumeChannelCount, coreaudio.iaudioendpointoffloadstreamvolume_getvolumechannelcount
f1_keywords:
- audioengineendpoint/IAudioEndpointOffloadStreamVolume.GetVolumeChannelCount
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
- IAudioEndpointOffloadStreamVolume.GetVolumeChannelCount
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/audioengineendpoint/nn-audioengineendpoint-iaudioendpointoffloadstreamvolume">IAudioEndpointOffloadStreamVolume</a>
 

 


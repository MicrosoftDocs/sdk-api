---
UID: NF:endpointvolume.IAudioEndpointVolume.GetMasterVolumeLevel
title: IAudioEndpointVolume::GetMasterVolumeLevel
author: windows-sdk-content
description: The GetMasterVolumeLevel method gets the master volume level, in decibels, of the audio stream that enters or leaves the audio endpoint device.
old-location: coreaudio\iaudioendpointvolume_getmastervolumelevel.htm
tech.root: CoreAudio
ms.assetid: 26e208e1-2291-4db6-857d-00b25d8fa343
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: GetMasterVolumeLevel, GetMasterVolumeLevel method [Core Audio], GetMasterVolumeLevel method [Core Audio],IAudioEndpointVolume interface, IAudioEndpointVolume interface [Core Audio],GetMasterVolumeLevel method, IAudioEndpointVolume.GetMasterVolumeLevel, IAudioEndpointVolume::GetMasterVolumeLevel, IAudioEndpointVolumeGetMasterVolumeLevel, coreaudio.iaudioendpointvolume_getmastervolumelevel, endpointvolume/IAudioEndpointVolume::GetMasterVolumeLevel
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: endpointvolume.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - Endpointvolume.h
api_name:
 - IAudioEndpointVolume.GetMasterVolumeLevel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAudioEndpointVolume::GetMasterVolumeLevel


## -description



The <b>GetMasterVolumeLevel</b> method gets the master volume level, in decibels, of the audio stream that enters or leaves the audio endpoint device.




## -parameters




### -param pfLevelDB [out]

Pointer to the master volume level. This parameter points to a <b>float</b> variable into which the method writes the volume level in decibels. To get the range of volume levels obtained from this method, call the <a href="https://msdn.microsoft.com/a0e98ed8-36e2-4abc-aa83-008cc89e3a56">IAudioEndpointVolume::GetVolumeRange</a> method.


## -returns



If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>pfLevelDB</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5e3e7ffc-8822-4b1b-b9af-206ec1e767e2">IAudioEndpointVolume Interface</a>



<a href="https://msdn.microsoft.com/a0e98ed8-36e2-4abc-aa83-008cc89e3a56">IAudioEndpointVolume::GetVolumeRange</a>
 

 


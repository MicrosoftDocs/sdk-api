---
UID: NF:endpointvolume.IAudioEndpointVolume.GetVolumeStepInfo
title: IAudioEndpointVolume::GetVolumeStepInfo
author: windows-sdk-content
description: The GetVolumeStepInfo method gets information about the current step in the volume range.
old-location: coreaudio\iaudioendpointvolume_getvolumestepinfo.htm
tech.root: CoreAudio
ms.assetid: 895f5dd1-73f5-464e-9498-b3832edf4dc7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetVolumeStepInfo, GetVolumeStepInfo method [Core Audio], GetVolumeStepInfo method [Core Audio],IAudioEndpointVolume interface, IAudioEndpointVolume interface [Core Audio],GetVolumeStepInfo method, IAudioEndpointVolume.GetVolumeStepInfo, IAudioEndpointVolume::GetVolumeStepInfo, IAudioEndpointVolumeGetVolumeStepInfo, coreaudio.iaudioendpointvolume_getvolumestepinfo, endpointvolume/IAudioEndpointVolume::GetVolumeStepInfo
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
 - IAudioEndpointVolume.GetVolumeStepInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAudioEndpointVolume::GetVolumeStepInfo


## -description



The <b>GetVolumeStepInfo</b> method gets information about the current step in the volume range.




## -parameters




### -param pnStep [out]

Pointer to a <b>UINT</b> variable into which the method writes the current step index. This index is a value in the range from 0 to <i>*pStepCount</i>– 1, where 0 represents the minimum volume level and <i>*pStepCount</i>– 1 represents the maximum level.


### -param pnStepCount [out]

Pointer to a <b>UINT</b> variable into which the method writes the number of steps in the volume range. This number remains constant for the lifetime of the <a href="https://msdn.microsoft.com/5e3e7ffc-8822-4b1b-b9af-206ec1e767e2">IAudioEndpointVolume</a> interface instance.


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
Parameter <i>pnStep</i> and <i>pnStepCount</i> are both <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



This method represents the volume level of the audio stream that enters or leaves the audio endpoint device as an index or "step" in a range of discrete volume levels. Output value <i>*pnStepCount</i> is the number of steps in the range. Output value <i>*pnStep</i> is the step index of the current volume level. If the number of steps is n = <i>*pnStepCount</i>, then step index <i>*pnStep</i> can assume values from 0 (minimum volume) to n – 1 (maximum volume).

Over the range from 0 to n – 1, successive intervals between adjacent steps do not necessarily represent uniform volume increments in either linear signal amplitude or decibels. In Windows Vista, <b>GetVolumeStepInfo</b> defines the relationship of index to volume level (signal amplitude) to be an audio-tapered curve. Note that the shape of the curve might change in future versions of Windows. For more information about audio-tapered curves, see <a href="https://msdn.microsoft.com/3b1adef5-40e9-4527-aa79-5a71f201fdfc">Audio-Tapered Volume Controls</a>.

Audio applications can call the <a href="https://msdn.microsoft.com/35ed44cd-ba91-4b6a-b528-0e22df389d31">IAudioEndpointVolume::VolumeStepUp</a> and <a href="https://msdn.microsoft.com/c334d780-784b-4fa3-bf4f-ea5d65459baf">IAudioEndpointVolume::VolumeStepDown</a> methods to increase or decrease the volume level by one interval. Either method first calculates the idealized volume level that corresponds to the next point on the audio-tapered curve. Next, the method selects the endpoint volume setting that is the best approximation to the idealized level. To obtain the range and granularity of the endpoint volume settings, call the <a href="https://msdn.microsoft.com/a0e98ed8-36e2-4abc-aa83-008cc89e3a56">IEndpointVolume::GetVolumeRange</a> method. If the audio endpoint device implements a hardware volume control, <b>GetVolumeRange</b> describes the hardware volume settings. Otherwise, the EndpointVolume API implements the endpoint volume control in software, and <b>GetVolumeRange</b> describes the volume settings of the software-implemented control.




## -see-also




<a href="https://msdn.microsoft.com/5e3e7ffc-8822-4b1b-b9af-206ec1e767e2">IAudioEndpointVolume Interface</a>



<a href="https://msdn.microsoft.com/c334d780-784b-4fa3-bf4f-ea5d65459baf">IAudioEndpointVolume::VolumeStepDown</a>



<a href="https://msdn.microsoft.com/35ed44cd-ba91-4b6a-b528-0e22df389d31">IAudioEndpointVolume::VolumeStepUp</a>
 

 


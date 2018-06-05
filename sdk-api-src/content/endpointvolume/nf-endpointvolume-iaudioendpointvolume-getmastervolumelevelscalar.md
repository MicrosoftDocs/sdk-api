---
UID: NF:endpointvolume.IAudioEndpointVolume.GetMasterVolumeLevelScalar
title: IAudioEndpointVolume::GetMasterVolumeLevelScalar
author: windows-sdk-content
description: The GetMasterVolumeLevelScalar method gets the master volume level of the audio stream that enters or leaves the audio endpoint device. The volume level is expressed as a normalized, audio-tapered value in the range from 0.0 to 1.0.
old-location: coreaudio\iaudioendpointvolume_getmastervolumelevelscalar.htm
old-project: CoreAudio
ms.assetid: 5a127507-99d2-48e8-b7e9-8bb51ff89f50
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetMasterVolumeLevelScalar, GetMasterVolumeLevelScalar method [Core Audio], GetMasterVolumeLevelScalar method [Core Audio],IAudioEndpointVolume interface, IAudioEndpointVolume interface [Core Audio],GetMasterVolumeLevelScalar method, IAudioEndpointVolume.GetMasterVolumeLevelScalar, IAudioEndpointVolume::GetMasterVolumeLevelScalar, IAudioEndpointVolumeGetMasterVolumeLevelScalar, coreaudio.iaudioendpointvolume_getmastervolumelevelscalar, endpointvolume/IAudioEndpointVolume::GetMasterVolumeLevelScalar
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: endpointvolume.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
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
req.typenames: ProtType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Endpointvolume.h
api_name:
-	IAudioEndpointVolume.GetMasterVolumeLevelScalar
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IAudioEndpointVolume::GetMasterVolumeLevelScalar


## -description



The <b>GetMasterVolumeLevelScalar</b> method gets the master volume level of the audio stream that enters or leaves the audio endpoint device. The volume level is expressed as a normalized, audio-tapered value in the range from 0.0 to 1.0.




## -parameters




### -param pfLevel [out]

Pointer to the master volume level. This parameter points to a <b>float</b> variable into which the method writes the volume level. The level is expressed as a normalized value in the range from 0.0 to 1.0.


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
Parameter <i>pfLevel</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The volume level is normalized to the range from 0.0 to 1.0, where 0.0 is the minimum volume level and 1.0 is the maximum level. Within this range, the relationship of the normalized volume level to the attenuation of signal amplitude is described by a nonlinear, audio-tapered curve. Note that the shape of the curve might change in future versions of Windows. For more information about audio-tapered curves, see <a href="https://msdn.microsoft.com/3b1adef5-40e9-4527-aa79-5a71f201fdfc">Audio-Tapered Volume Controls</a>.

The normalized volume levels that are retrieved by this method are suitable to represent the positions of volume controls in application windows and on-screen displays.

For a code example that calls <b>GetMasterVolumeLevelScalar</b>, see <a href="https://msdn.microsoft.com/667c3659-69ae-469d-9ae0-e32a189cbc71">Endpoint Volume Controls</a>.




## -see-also




<a href="https://msdn.microsoft.com/5e3e7ffc-8822-4b1b-b9af-206ec1e767e2">IAudioEndpointVolume Interface</a>
 

 


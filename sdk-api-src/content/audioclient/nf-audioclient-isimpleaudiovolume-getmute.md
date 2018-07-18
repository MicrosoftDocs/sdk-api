---
UID: NF:audioclient.ISimpleAudioVolume.GetMute
title: ISimpleAudioVolume::GetMute
author: windows-sdk-content
description: The GetMute method retrieves the current muting state for the audio session.
old-location: coreaudio\isimpleaudiovolume_getmute.htm
old-project: CoreAudio
ms.assetid: 35890423-2aac-473b-a820-ba7cb1b5e05e
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: GetMute, GetMute method [Core Audio], GetMute method [Core Audio],ISimpleAudioVolume interface, ISimpleAudioVolume interface [Core Audio],GetMute method, ISimpleAudioVolume.GetMute, ISimpleAudioVolume::GetMute, ISimpleAudioVolumeGetMute, audioclient/ISimpleAudioVolume::GetMute, coreaudio.isimpleaudiovolume_getmute
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: audioclient.h
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audioclient.h
api_name:
 - ISimpleAudioVolume.GetMute
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ISimpleAudioVolume::GetMute


## -description



The <b>GetMute</b> method retrieves the current muting state for the audio session.




## -parameters




### -param pbMute [out]

Pointer to a <b>BOOL</b> variable into which the method writes the muting state. <b>TRUE</b> indicates that muting is enabled. <b>FALSE</b> indicates that it is disabled.


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
Parameter <i>pbMute</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_DEVICE_INVALIDATED</b></dt>
</dl>
</td>
<td width="60%">
The audio endpoint device has been unplugged, or the audio hardware or associated hardware resources have been reconfigured, disabled, removed, or otherwise made unavailable for use.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_SERVICE_NOT_RUNNING</b></dt>
</dl>
</td>
<td width="60%">
The Windows audio service is not running.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/0d0a20dc-5e5a-49a7-adc9-20aacb88368a">IChannelAudioVolume Interface</a>



<a href="https://msdn.microsoft.com/360211f2-de82-4ff5-896c-dee1d60cb7b7">ISimpleAudioVolume Interface</a>



<a href="https://msdn.microsoft.com/64fc7146-8d4b-429c-bf35-c43e31a41af8">ISimpleAudioVolume::SetMute</a>
 

 


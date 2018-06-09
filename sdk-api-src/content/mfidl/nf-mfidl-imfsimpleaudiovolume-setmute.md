---
UID: NF:mfidl.IMFSimpleAudioVolume.SetMute
title: IMFSimpleAudioVolume::SetMute
author: windows-sdk-content
description: Mutes or unmutes the audio.
old-location: mf\imfsimpleaudiovolume_setmute.htm
old-project: medfound
ms.assetid: d8840d15-d4d5-481e-9002-54fdbf323c9c
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: IMFSimpleAudioVolume interface [Media Foundation],SetMute method, IMFSimpleAudioVolume.SetMute, IMFSimpleAudioVolume::SetMute, SetMute, SetMute method [Media Foundation], SetMute method [Media Foundation],IMFSimpleAudioVolume interface, d8840d15-d4d5-481e-9002-54fdbf323c9c, mf.imfsimpleaudiovolume_setmute, mfidl/IMFSimpleAudioVolume::SetMute
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: MFSensorDeviceMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFSimpleAudioVolume.SetMute
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSimpleAudioVolume::SetMute


## -description



Mutes or unmutes the audio.




## -parameters




### -param bMute [in]

Specify <b>TRUE</b> to mute the audio, or <b>FALSE</b> to unmute the audio.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The audio renderer is not initialized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_STREAMSINK_REMOVED</b></dt>
</dl>
</td>
<td width="60%">
The audio renderer was removed from the pipeline.

</td>
</tr>
</table>
 




## -remarks



This method does not change the volume level returned by the <a href="https://msdn.microsoft.com/03ce097e-c4e5-4dac-84c0-b569efc420bc">IMFSimpleAudioVolume::GetMasterVolume</a> function.




## -see-also




<a href="https://msdn.microsoft.com/002d85a7-8bc3-422e-8ced-1907ac121d7b">IMFSimpleAudioVolume</a>



<a href="https://msdn.microsoft.com/5884a128-597d-432b-a706-e10c894d7965">Streaming Audio Renderer</a>
 

 


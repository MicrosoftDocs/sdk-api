---
UID: NF:mfidl.IMFSimpleAudioVolume.SetMasterVolume
title: IMFSimpleAudioVolume::SetMasterVolume
author: windows-sdk-content
description: Sets the master volume level.
old-location: mf\imfsimpleaudiovolume_setmastervolume.htm
tech.root: medfound
ms.assetid: 42b51817-3c2a-463a-a533-19c327c57354
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: 42b51817-3c2a-463a-a533-19c327c57354, IMFSimpleAudioVolume interface [Media Foundation],SetMasterVolume method, IMFSimpleAudioVolume.SetMasterVolume, IMFSimpleAudioVolume::SetMasterVolume, SetMasterVolume, SetMasterVolume method [Media Foundation], SetMasterVolume method [Media Foundation],IMFSimpleAudioVolume interface, mf.imfsimpleaudiovolume_setmastervolume, mfidl/IMFSimpleAudioVolume::SetMasterVolume
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFSimpleAudioVolume.SetMasterVolume
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSimpleAudioVolume::SetMasterVolume


## -description



Sets the master volume level.




## -parameters




### -param fLevel [in]

Volume level. Volume is expressed as an attenuation level, where 0.0 indicates silence and 1.0 indicates full volume (no attenuation).


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



Events outside of the application can change the master volume level. For example, the user can change the volume from the system volume-control program (SndVol). If an external event changes the master volume, the audio renderer sends an <a href="https://msdn.microsoft.com/63c37bd2-0289-407a-92f1-169eb5d2e02e">MEAudioSessionVolumeChanged</a> event, which the Media Session forwards to the application.




## -see-also




<a href="https://msdn.microsoft.com/002d85a7-8bc3-422e-8ced-1907ac121d7b">IMFSimpleAudioVolume</a>



<a href="https://msdn.microsoft.com/5884a128-597d-432b-a706-e10c894d7965">Streaming Audio Renderer</a>
 

 


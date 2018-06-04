---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IDirectMusicSynth::Activate


## -description


The <code>Activate</code> method enables or disables the audio device under program control.


## -parameters




### -param fEnable

Specifies whether to enable or disable the audio device. If <b>TRUE</b>, the method enables the device. If <b>FALSE</b>, the method disables it.


## -returns



<code>Activate</code> returns S_OK if the call was successful. Otherwise, the method returns an appropriate error code. The following table shows some of the possible return status codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Indicates audio device is already inactive.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the request failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Indicates that not enough memory is available to load the device.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMUS_E_SYNTHNOTCONFIGURED</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the synth is not opened or not properly configured.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMUS_E_NOSYNTHSINK</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the <b>IDirectMusicSynthSink</b> object was not connected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMUS_E_SYNTHACTIVE</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the synth is already active.

</td>
</tr>
</table>
 




## -remarks



By enabling or disabling the audio device under program control, <code>Activate</code> gives the application the ability to manage its use of resources. When not playing music, the application can deactivate the wave-output resource, which frees it for other applications to use.

The wave-output resource is actually managed by a separate COM object, which has a <a href="https://msdn.microsoft.com/library/windows/hardware/ff536520">IDirectMusicSynthSink</a> interface. This object must first be connected with a call to <b>SetSynthSink</b>. Otherwise, the synthesizer will fail the <code>Activate</code> call with DMUS_E_NOSYNTHSINK.

Activation is mostly managed by the wave sink object. When <code>IDirectMusicSynth::Activate</code> is called, the synth sets its internal activation state and calls <a href="https://msdn.microsoft.com/library/windows/hardware/ff536521">IDirectMusicSynthSink::Activate</a> to enable or disable the wave output.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff536539">IDirectMusicSynth::Open</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff536521">IDirectMusicSynthSink::Activate</a>
 

 


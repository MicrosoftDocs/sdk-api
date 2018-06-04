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

# IDirectMusicSynthSink::Activate


## -description


The <code>Activate</code> method activates or deactivates the synthesizer sink.


## -parameters




### -param fEnable

Specifies whether to activate the synth sink. If <b>TRUE</b>, the method activates the synth sink. If <b>FALSE</b>, it deactivates it.


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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the method is unable to activate or deactivate the synth sink.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMUS_E_SYNTHNOTCONFIGURED</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the synth is not set or not properly configured.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMUS_E_SYNTHACTIVE</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the sink is already active.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMUS_E_DSOUND_NOT_SET</b></dt>
</dl>
</td>
<td width="60%">
Indicates that <b>SetDirectSound</b> hasn't been called successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMUS_E_NO_MASTER_CLOCK</b></dt>
</dl>
</td>
<td width="60%">
Indicates that <b>SetMasterClock</b> hasn't been called successfully.

</td>
</tr>
</table>
 




## -remarks



The synthesizer itself can be told to enable or disable the audio device. In turn, it calls the synth sink, which manages the audio device. This gives the application the ability to manage its use of resources. When it is not playing music, it can deactivate the sink to free the wave-output device for other applications.

For more information, see the description of the <b>IDirectMusic</b> interface in the Microsoft Windows SDK documentation.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff536519">IDirectMusicSynth</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff536529">IDirectMusicSynth::Activate</a>
 

 


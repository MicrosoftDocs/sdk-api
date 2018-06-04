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

# IDirectMusicSynthSink::SetDirectSound


## -description


The <code>SetDirectSound</code> method connects the synthesizer sink with an existing DirectSound object and a DirectSound buffer.


## -parameters




### -param pDirectSound

Pointer to an <b>IDirectSound</b> object that the sink is to be associated with. This parameter is set to a valid, non-<b>NULL</b> pointer value.


### -param pDirectSoundBuffer

Pointer to the <b>IDirectSoundBuffer</b> object that the sink is to be associated with. This parameter can be <b>NULL</b>. For more information, see the following Remarks section.


## -returns



<code>SetDirectSound</code> returns S_OK if the call was successful. Otherwise, the method returns an appropriate error code. The following table shows some of the possible return status codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMUS_E_SYNTHNOTCONFIGURED</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the synth not set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMUS_E_SYNTHACTIVE</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the sink is active.

</td>
</tr>
</table>
 




## -remarks



The <i>pDirectSound</i> parameter points to an <b>IDirectSound</b> instance that is received from <code>IDirectMusicPort::SetDirectSound</code> and is non-<b>NULL</b>.

If <i>pDirectSoundBuffer</i> is <b>NULL</b>, the primary buffer for <b>IDirectSound</b> will be upgraded, if necessary, to support the sample rate and channel information for the sink (obtained from <a href="https://msdn.microsoft.com/library/windows/hardware/ff536535">IDirectMusicSynth::GetFormat</a>).

The <b>IDirectSoundBuffer</b> should be a secondary streaming buffer with a format that matches the format obtained from the synthesizer. If <i>pDirectSoundBuffer</i> is <b>NULL</b>, then an appropriate <b>IDirectSoundBuffer</b> instance will be created internally.

Neither the <b>IDirectSound</b> nor the <b>IDirectSoundBuffer</b> instance can be changed once the sink has been activated.

The <i>pDirectSound</i> and <i>pDirectSoundBuffer</i> parameters follow the <a href="https://msdn.microsoft.com/e6b19110-37e2-4d23-a528-6393c12ab650">reference-counting conventions for COM objects</a>.

For more information, see the description of the <b>IDirectSound</b>, <b>IDirectSoundBuffer</b>, and <b>IDirectMusicPort</b> interfaces in the Microsoft Windows SDK documentation.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff536535">IDirectMusicSynth::GetFormat</a>
 

 


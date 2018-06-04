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

# IDirectMusicSynth::SetSynthSink


## -description


The <code>SetSynthSink</code> method establishes the connection of the synth to the wave sink.


## -parameters




### -param pSynthSink

Pointer to the synth sink. This parameter either points to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff536520">IDirectMusicSynthSink</a> sink object to connect to the synth, or is <b>NULL</b> to disconnect the synth from its current synth sink.


## -returns



<code>SetSynthSink</code> returns S_OK if the call was successful. Otherwise, the method returns an appropriate error code. The following table shows some of the possible return status codes.

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
Indicates that a bad pointer was passed in <i>pSynthSink</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the method failed because it was unable to connect to the <b>IDirectMusicSynthSink</b> object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Indicates that not enough memory is available to establish the connection.

</td>
</tr>
</table>
 




## -remarks



Before the synthesizer can expose much of its functionality, it must be connected to a wave sink object, which is represented by the <b>IDirectMusicSynthSink</b> interface. The <code>IDirectMusicSynth::SetSynthSink</code> method establishes this connection.

The <b>IDirectMusicSynthSink</b> object does the work of actually connecting up to the ultimate audio destination, which might be DirectSound, Microsoft Win32 wave audio, or some other audio stream. The default implementation sends data to DirectSound.

This approach allows a synthesizer to connect to many different styles of audio out without special code within the synthesizer itself. This makes it very easy to connect one synthesizer implementation to any available wave-output device.

For more information, see the description of the <b>IDirectMusic</b> interface in the Microsoft Windows SDK documentation.

The <i>pSynthSink</i> parameter follows the <a href="https://msdn.microsoft.com/e6b19110-37e2-4d23-a528-6393c12ab650">reference-counting conventions for COM objects</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff536520">IDirectMusicSynthSink</a>
 

 


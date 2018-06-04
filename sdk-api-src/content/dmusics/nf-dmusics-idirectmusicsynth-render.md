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

# IDirectMusicSynth::Render


## -description


The <code>Render</code> method is called by the synth sink to render to a buffer in the audio stream.


## -parameters




### -param pBuffer

Pointer to the buffer to write to


### -param dwLength

Specifies the length of the buffer. The buffer length is expressed in samples, not bytes. The size in bytes of the buffer can vary, depending on the buffer's format, which the synth sets in response to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff536529">IDirectMusicSynth::Activate</a> command.


### -param llPosition






#### - dwPosition

Specifies the position in the audio stream. The position is expressed in samples, not bytes. The caller should always increment this value by <i>dwLength</i> after each call.


## -returns



<code>Render</code> returns S_OK if the call was successful. Otherwise, the method returns an appropriate error code. The following table shows some of the possible return status codes.

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
Indicates that the method failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Indicates a bad buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMUS_E_SYNTHNOTCONFIGURED</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the synth is not open or not properly configured.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMUS_E_SYNTHINACTIVE</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the method is not valid when synth is inactive.

</td>
</tr>
</table>
 




## -remarks



Typically, a synthesizer manages converting messages into rendered wave data in two processes. In the first, it time stamps the MIDI messages it receives from the application via calls to <a href="https://msdn.microsoft.com/library/windows/hardware/ff536540">IDirectMusicSynth::PlayBuffer</a> and places them in its own internal queue. Then, in response to <code>Render</code>, the second process generates audio by pulling MIDI messages from the queue and synthesizing the appropriate tones within the time span of the requested render buffer.

As the synthesizer renders the MIDI messages into the buffer, it calls <a href="https://msdn.microsoft.com/library/windows/hardware/ff536525">IDirectMusicSynthSink::RefTimeToSample</a> to translate the MIDI time stamps into sample positions. This guarantees extremely accurate timing (as long as the <b>IDirectMusicSynthSink</b> implementation is well written).

For more information, see the description of the <b>IDirectMusic</b> interface in the Microsoft Windows SDK documentation.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff536529">IDirectMusicSynth::Activate</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff536540">IDirectMusicSynth::PlayBuffer</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff536525">IDirectMusicSynthSink::RefTimeToSample</a>
 

 


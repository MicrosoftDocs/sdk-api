---
UID: NF:dmusics.IDirectMusicSynth.Render
title: IDirectMusicSynth::Render
author: windows-sdk-content
description: The Render method is called by the synth sink to render to a buffer in the audio stream.
old-location: audio\idirectmusicsynth_render.htm
tech.root: audio
ms.assetid: c0aea93c-df92-46e6-9cd7-38235f513924
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: IDirectMusicSynth interface [Audio Devices],Render method, IDirectMusicSynth.Render, IDirectMusicSynth::Render, Render, Render method [Audio Devices], Render method [Audio Devices],IDirectMusicSynth interface, audio.idirectmusicsynth_render, audmp-routines_fd2bebe8-7170-4222-b465-b1a9799abf8e.xml, dmusics/IDirectMusicSynth::Render
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dmusics.h
req.include-header: Dmusics.h
req.target-type: Desktop
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dmusics.h
api_name:
 - IDirectMusicSynth.Render
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectMusicSynth::Render


## -description


The <code>Render</code> method is called by the synth sink to render to a buffer in the audio stream.


## -parameters




### -param pBuffer

Pointer to the buffer to write to


### -param dwLength

Specifies the length of the buffer. The buffer length is expressed in samples, not bytes. The size in bytes of the buffer can vary, depending on the buffer's format, which the synth sets in response to an <a href="https://msdn.microsoft.com/9efdb079-ed24-43b4-844b-344571399de7">IDirectMusicSynth::Activate</a> command.


### -param llPosition

TBD




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



Typically, a synthesizer manages converting messages into rendered wave data in two processes. In the first, it time stamps the MIDI messages it receives from the application via calls to <a href="https://msdn.microsoft.com/96d0a2ef-1265-4e04-bb70-920f4c82058c">IDirectMusicSynth::PlayBuffer</a> and places them in its own internal queue. Then, in response to <code>Render</code>, the second process generates audio by pulling MIDI messages from the queue and synthesizing the appropriate tones within the time span of the requested render buffer.

As the synthesizer renders the MIDI messages into the buffer, it calls <a href="https://msdn.microsoft.com/11a6b670-93d6-4455-b279-a1fc5fca0d1d">IDirectMusicSynthSink::RefTimeToSample</a> to translate the MIDI time stamps into sample positions. This guarantees extremely accurate timing (as long as the <b>IDirectMusicSynthSink</b> implementation is well written).

For more information, see the description of the <b>IDirectMusic</b> interface in the Microsoft Windows SDK documentation.




## -see-also




<a href="https://msdn.microsoft.com/9efdb079-ed24-43b4-844b-344571399de7">IDirectMusicSynth::Activate</a>



<a href="https://msdn.microsoft.com/96d0a2ef-1265-4e04-bb70-920f4c82058c">IDirectMusicSynth::PlayBuffer</a>



<a href="https://msdn.microsoft.com/11a6b670-93d6-4455-b279-a1fc5fca0d1d">IDirectMusicSynthSink::RefTimeToSample</a>
 

 


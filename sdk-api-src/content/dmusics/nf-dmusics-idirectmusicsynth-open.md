---
UID: NF:dmusics.IDirectMusicSynth.Open
title: IDirectMusicSynth::Open method
author: windows-driver-content
description: The Open method opens a DirectMusic synthesizer &#0034;port&#0034;.
old-location: audio\idirectmusicsynth_open.htm
old-project: audio
ms.assetid: 15a16b27-7693-4fc6-80ae-e8aedcf879d0
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: IDirectMusicSynth, IDirectMusicSynth interface [Audio Devices], Open method, IDirectMusicSynth::Open, Open method [Audio Devices], Open method [Audio Devices], IDirectMusicSynth interface, Open,IDirectMusicSynth.Open, audio.idirectmusicsynth_open, audmp-routines_5bb9c701-4377-42fb-91ac-733952708a38.xml, dmusics/IDirectMusicSynth::Open
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
req.typenames: DMO_PARTIAL_MEDIATYPE, *PDMO_PARTIAL_MEDIATYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dmusics.h
api_name:
-	IDirectMusicSynth.Open
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectMusicSynth::Open method


## -description


The <code>Open</code> method opens a DirectMusic synthesizer "port".


## -parameters




### -param pPortParams

Pointer to a DMUS_PORTPARAMS structure (described in the Microsoft Windows SDK documentation) specifying a set of options for opening the DirectMusic "port". The structure contains setup parameters for the port, including sample rate, stereo mode, and number of voices. If this parameter is set to <b>NULL</b>, default settings are used.


## -returns



<code>Open</code> returns S_OK if the call was successful. Otherwise, the method returns an appropriate error code. The following table shows some of the possible return status codes.

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
Indicates a bad pointer was passed in <i>pPortParams</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMUS_E_ALREADYOPEN</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the port was already opened.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMUS_E_NOSYNTHSINK</b></dt>
</dl>
</td>
<td width="60%">
Indicates that no sink is available for output.

</td>
</tr>
</table>
 




## -remarks



The DirectMusic synthesizer "port" can be opened only once. A second attempt to open the port will fail.

However, DirectMusic does support multiple instances of a synthesizer port. It does this by calling <b>CoCreateInstance</b> (described in the Windows SDK documentation) to create multiple <b>IDirectMusicSynth</b> objects.

The port is valid until it is closed by the <a href="https://msdn.microsoft.com/library/windows/hardware/ff536531">IDirectMusicSynth::Close</a> method.

When opening the port, some of the parameters asked for in DMUS_PORTPARAMS might not be supported or the port might "upgrade" a parameter request (that is, return the maximum number of voices supported instead of just what was asked for). In either of these cases, the Microsoft Software Synthesizer will return S_FALSE and modify DMUS_PORTPARAMS accordingly, to show what is actually supported. Custom synths should emulate this behavior to ensure compatibility with existing code.

Opening a port is not enough to enable the synthesizer. The synthesizer is enabled by opening the port and enabling audio output through <a href="https://msdn.microsoft.com/library/windows/hardware/ff536529">IDirectMusicSynth::Activate</a>.

Avoid confusing the term DirectMusic "port" with a DMus port driver. A DirectMusic port corresponds to a render or capture pin on a DirectMusic filter. For more information about DirectMusic ports, see the description of the <b>IDirectMusicPort</b> interface in the Windows SDK documentation.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff536529">IDirectMusicSynth::Activate</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff536531">IDirectMusicSynth::Close</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff536532">IDirectMusicSynth::Download</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff536540">IDirectMusicSynth::PlayBuffer</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff536546">IDirectMusicSynth::Unload</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff536520">IDirectMusicSynthSink</a>
 

 


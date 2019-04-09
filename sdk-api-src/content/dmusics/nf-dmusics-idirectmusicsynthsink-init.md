---
UID: NF:dmusics.IDirectMusicSynthSink.Init
title: IDirectMusicSynthSink::Init (dmusics.h)
author: windows-sdk-content
description: The Init method initializes the synth-sink object.
old-location: audio\idirectmusicsynthsink_init.htm
tech.root: audio
ms.assetid: d390c54d-18f6-47e1-9d52-057c984d284a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDirectMusicSynthSink interface [Audio Devices],Init method, IDirectMusicSynthSink.Init, IDirectMusicSynthSink::Init, Init, Init method [Audio Devices], Init method [Audio Devices],IDirectMusicSynthSink interface, audio.idirectmusicsynthsink_init, audmp-routines_d4f2d6c1-4bb6-453e-ad40-d0daab7775a3.xml, dmusics/IDirectMusicSynthSink::Init
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
 - IDirectMusicSynthSink.Init
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectMusicSynthSink::Init


## -description


The <code>Init</code> method initializes the synth-sink object.


## -parameters




### -param pSynth

Pointer to the synth object that the synth-sink object is to connect to. This parameter is a valid, non-NULL pointer to a <a href="https://msdn.microsoft.com/08f1056a-fead-475b-a13a-ee11b9709241">IDirectMusicSynth</a> object.


## -returns



<code>Init</code> returns S_OK if the call is successful. Otherwise, the method returns an appropriate error code.




## -remarks



When a synthesizer is connected to a synth sink by a call to <a href="https://msdn.microsoft.com/51153ea3-7c61-458a-8879-10efbd678b53">IDirectMusicSynth::SetSynthSink</a>, the synthesizer calls the synth sink's <code>Init</code> method.

In order to avoid cyclical references, the <b>IDirectMusicSynthSink</b> does not increment the reference count of the <a href="https://msdn.microsoft.com/08f1056a-fead-475b-a13a-ee11b9709241">IDirectMusicSynth</a> synth object. Instead, it abides by the rule that <b>IDirectMusicSynth</b> object is always the parent and always releases the <b>IDirectMusicSynthSink</b> object when it is done with it.

Once connected, the synth sink needs to be activated with a call to <a href="https://msdn.microsoft.com/49b66410-23bd-4c4d-929c-b7e82fb45a9c">IDirectMusicSynthSink::Activate</a>. At this point it starts generating wave buffers, which it passes to the synthesizer by calling <a href="https://msdn.microsoft.com/c0aea93c-df92-46e6-9cd7-38235f513924">IDirectMusicSynth::Render</a>.

The <i>pSynth</i> parameter follows the <a href="https://msdn.microsoft.com/e6b19110-37e2-4d23-a528-6393c12ab650">reference-counting conventions for COM objects</a>.

For more information, see <a href="https://msdn.microsoft.com/ddcb847e-d46e-4860-9be9-4480e5a6b710">Synthesizers and Wave Sinks</a>. Also see the description of the <b>IDirectMusic</b> interface in the Microsoft Windows SDK documentation.




## -see-also




<a href="https://msdn.microsoft.com/08f1056a-fead-475b-a13a-ee11b9709241">IDirectMusicSynth</a>



<a href="https://msdn.microsoft.com/9efdb079-ed24-43b4-844b-344571399de7">IDirectMusicSynth::Activate</a>



<a href="https://msdn.microsoft.com/c0aea93c-df92-46e6-9cd7-38235f513924">IDirectMusicSynth::Render</a>



<a href="https://msdn.microsoft.com/51153ea3-7c61-458a-8879-10efbd678b53">IDirectMusicSynth::SetSynthSink</a>



<a href="https://msdn.microsoft.com/49b66410-23bd-4c4d-929c-b7e82fb45a9c">IDirectMusicSynthSink::Activate</a>
 

 


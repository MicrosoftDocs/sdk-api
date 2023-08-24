---
UID: NF:dmusics.IDirectMusicSynthSink.Init
title: IDirectMusicSynthSink::Init (dmusics.h)
description: The Init method initializes the synth-sink object.
helpviewer_keywords: ["IDirectMusicSynthSink interface [Audio Devices]","Init method","IDirectMusicSynthSink.Init","IDirectMusicSynthSink::Init","Init","Init method [Audio Devices]","Init method [Audio Devices]","IDirectMusicSynthSink interface","audio.idirectmusicsynthsink_init","audmp-routines_d4f2d6c1-4bb6-453e-ad40-d0daab7775a3.xml","dmusics/IDirectMusicSynthSink::Init"]
old-location: audio\idirectmusicsynthsink_init.htm
tech.root: dshow
ms.assetid: d390c54d-18f6-47e1-9d52-057c984d284a
ms.date: 12/05/2018
ms.keywords: IDirectMusicSynthSink interface [Audio Devices],Init method, IDirectMusicSynthSink.Init, IDirectMusicSynthSink::Init, Init, Init method [Audio Devices], Init method [Audio Devices],IDirectMusicSynthSink interface, audio.idirectmusicsynthsink_init, audmp-routines_d4f2d6c1-4bb6-453e-ad40-d0daab7775a3.xml, dmusics/IDirectMusicSynthSink::Init
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectMusicSynthSink::Init
 - dmusics/IDirectMusicSynthSink::Init
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dmusics.h
api_name:
 - IDirectMusicSynthSink.Init
archived: true
---

# IDirectMusicSynthSink::Init


## -description

The <code>Init</code> method initializes the synth-sink object.

## -parameters

### -param pSynth

Pointer to the synth object that the synth-sink object is to connect to. This parameter is a valid, non-NULL pointer to a <a href="/windows/desktop/api/dmusics/nn-dmusics-idirectmusicsynth">IDirectMusicSynth</a> object.

## -returns

<code>Init</code> returns S_OK if the call is successful. Otherwise, the method returns an appropriate error code.

## -remarks

When a synthesizer is connected to a synth sink by a call to <a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-setsynthsink">IDirectMusicSynth::SetSynthSink</a>, the synthesizer calls the synth sink's <code>Init</code> method.

In order to avoid cyclical references, the <b>IDirectMusicSynthSink</b> does not increment the reference count of the <a href="/windows/desktop/api/dmusics/nn-dmusics-idirectmusicsynth">IDirectMusicSynth</a> synth object. Instead, it abides by the rule that <b>IDirectMusicSynth</b> object is always the parent and always releases the <b>IDirectMusicSynthSink</b> object when it is done with it.

Once connected, the synth sink needs to be activated with a call to <a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynthsink-activate">IDirectMusicSynthSink::Activate</a>. At this point it starts generating wave buffers, which it passes to the synthesizer by calling <a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-render">IDirectMusicSynth::Render</a>.

The <i>pSynth</i> parameter follows the <a href="/windows-hardware/drivers/audio/reference-counting-conventions-for-com-objects">reference-counting conventions for COM objects</a>.

For more information, see <a href="/windows-hardware/drivers/audio/synthesizers-and-wave-sinks">Synthesizers and Wave Sinks</a>. Also see the description of the <b>IDirectMusic</b> interface in the Microsoft Windows SDK documentation.

## -see-also

<a href="/windows/desktop/api/dmusics/nn-dmusics-idirectmusicsynth">IDirectMusicSynth</a>



<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-activate">IDirectMusicSynth::Activate</a>



<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-render">IDirectMusicSynth::Render</a>



<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-setsynthsink">IDirectMusicSynth::SetSynthSink</a>



<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynthsink-activate">IDirectMusicSynthSink::Activate</a>
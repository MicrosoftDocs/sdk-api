---
UID: NN:dmusics.IDirectMusicSynth
title: IDirectMusicSynth (dmusics.h)
description: The IDirectMusicSynth interface is used by DirectMusic to communicate with user-mode synthesizers.
helpviewer_keywords: ["IDirectMusicSynth","IDirectMusicSynth interface [Audio Devices]","IDirectMusicSynth interface [Audio Devices]","described","audio.idirectmusicsynth","audmp-routines_ab253bc7-f9a6-4279-99fb-4e5b2693c94b.xml","dmusics/IDirectMusicSynth"]
old-location: audio\idirectmusicsynth.htm
tech.root: dshow
ms.assetid: 08f1056a-fead-475b-a13a-ee11b9709241
ms.date: 12/05/2018
ms.keywords: IDirectMusicSynth, IDirectMusicSynth interface [Audio Devices], IDirectMusicSynth interface [Audio Devices],described, audio.idirectmusicsynth, audmp-routines_ab253bc7-f9a6-4279-99fb-4e5b2693c94b.xml, dmusics/IDirectMusicSynth
req.header: dmusics.h
req.include-header: 
req.target-type: Windows
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
 - IDirectMusicSynth
 - dmusics/IDirectMusicSynth
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
 - IDirectMusicSynth
archived: true
---

# IDirectMusicSynth interface


## -description

The <code>IDirectMusicSynth</code> interface is used by DirectMusic to communicate with user-mode synthesizers. If you create a custom software synthesizer that runs in user mode, it should have an <code>IDirectMusicSynth</code> interface to plug into DirectMusic. <code>IDirectMusicSynth</code> inherits from the <b>IUnknown</b> interface.

The synthesizer is not complete without a connection to a wave sink, which is represented as an object with an <a href="/windows/desktop/api/dmusics/nn-dmusics-idirectmusicsynthsink">IDirectMusicSynthSink</a> interface. For more information, see <a href="/windows-hardware/drivers/audio/idirectmusicsynth-and-idirectmusicsynthsink">IDirectMusicSynth and IDirectMusicSynthSink</a>.

In addition to the methods that <code>IDirectMusicSynth</code> inherits from the <b>IUnknown</b> interface, <code>IDirectMusicSynth</code> supports the following methods:
<dl>
<dd>

<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-activate">IDirectMusicSynth::Activate</a>


</dd>
<dd>

<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-close">IDirectMusicSynth::Close</a>


</dd>
<dd>

<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-download">IDirectMusicSynth::Download</a>


</dd>
<dd>

<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-getappend">IDirectMusicSynth::GetAppend</a>


</dd>
<dd>

<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-getchannelpriority">IDirectMusicSynth::GetChannelPriority</a>


</dd>
<dd>

<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-getformat">IDirectMusicSynth::GetFormat</a>


</dd>
<dd>

<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-getlatencyclock">IDirectMusicSynth::GetLatencyClock</a>


</dd>
<dd>

<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-getportcaps">IDirectMusicSynth::GetPortCaps</a>


</dd>
<dd>

<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-getrunningstats">IDirectMusicSynth::GetRunningStats</a>


</dd>
<dd>

<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-open">IDirectMusicSynth::Open</a>


</dd>
<dd>

<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-playbuffer">IDirectMusicSynth::PlayBuffer</a>


</dd>
<dd>

<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-render">IDirectMusicSynth::Render</a>


</dd>
<dd>

<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-setchannelpriority">IDirectMusicSynth::SetChannelPriority</a>


</dd>
<dd>

<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-setmasterclock">IDirectMusicSynth::SetMasterClock</a>


</dd>
<dd>

<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-setnumchannelgroups">IDirectMusicSynth::SetNumChannelGroups</a>


</dd>
<dd>

<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-setsynthsink">IDirectMusicSynth::SetSynthSink</a>


</dd>
<dd>

<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-unload">IDirectMusicSynth::Unload</a>


</dd>
</dl>
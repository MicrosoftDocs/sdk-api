---
UID: NF:dmusics.IDirectMusicSynthSink.Activate
title: IDirectMusicSynthSink::Activate (dmusics.h)
description: The Activate method activates or deactivates the synthesizer sink.
helpviewer_keywords: ["Activate","Activate method [Audio Devices]","Activate method [Audio Devices]","IDirectMusicSynthSink interface","IDirectMusicSynthSink interface [Audio Devices]","Activate method","IDirectMusicSynthSink.Activate","IDirectMusicSynthSink::Activate","audio.idirectmusicsynthsink_activate","audmp-routines_8a2d5dd7-92f1-4341-a5f3-68fd1215fc06.xml","dmusics/IDirectMusicSynthSink::Activate"]
old-location: audio\idirectmusicsynthsink_activate.htm
tech.root: dshow
ms.assetid: 49b66410-23bd-4c4d-929c-b7e82fb45a9c
ms.date: 12/05/2018
ms.keywords: Activate, Activate method [Audio Devices], Activate method [Audio Devices],IDirectMusicSynthSink interface, IDirectMusicSynthSink interface [Audio Devices],Activate method, IDirectMusicSynthSink.Activate, IDirectMusicSynthSink::Activate, audio.idirectmusicsynthsink_activate, audmp-routines_8a2d5dd7-92f1-4341-a5f3-68fd1215fc06.xml, dmusics/IDirectMusicSynthSink::Activate
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
 - IDirectMusicSynthSink::Activate
 - dmusics/IDirectMusicSynthSink::Activate
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
 - IDirectMusicSynthSink.Activate
archived: true
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

<a href="/windows/desktop/api/dmusics/nn-dmusics-idirectmusicsynth">IDirectMusicSynth</a>



<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-activate">IDirectMusicSynth::Activate</a>
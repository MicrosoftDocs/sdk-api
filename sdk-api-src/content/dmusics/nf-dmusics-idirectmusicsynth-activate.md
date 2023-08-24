---
UID: NF:dmusics.IDirectMusicSynth.Activate
title: IDirectMusicSynth::Activate (dmusics.h)
description: The Activate method enables or disables the audio device under program control.
helpviewer_keywords: ["Activate","Activate method [Audio Devices]","Activate method [Audio Devices]","IDirectMusicSynth interface","IDirectMusicSynth interface [Audio Devices]","Activate method","IDirectMusicSynth.Activate","IDirectMusicSynth::Activate","audio.idirectmusicsynth_activate","audmp-routines_56894d17-83db-4b4f-8e26-58103856a97e.xml","dmusics/IDirectMusicSynth::Activate"]
old-location: audio\idirectmusicsynth_activate.htm
tech.root: dshow
ms.assetid: 9efdb079-ed24-43b4-844b-344571399de7
ms.date: 12/05/2018
ms.keywords: Activate, Activate method [Audio Devices], Activate method [Audio Devices],IDirectMusicSynth interface, IDirectMusicSynth interface [Audio Devices],Activate method, IDirectMusicSynth.Activate, IDirectMusicSynth::Activate, audio.idirectmusicsynth_activate, audmp-routines_56894d17-83db-4b4f-8e26-58103856a97e.xml, dmusics/IDirectMusicSynth::Activate
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
 - IDirectMusicSynth::Activate
 - dmusics/IDirectMusicSynth::Activate
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
 - IDirectMusicSynth.Activate
archived: true
---

# IDirectMusicSynth::Activate


## -description

The <code>Activate</code> method enables or disables the audio device under program control.

## -parameters

### -param fEnable

Specifies whether to enable or disable the audio device. If <b>TRUE</b>, the method enables the device. If <b>FALSE</b>, the method disables it.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Indicates audio device is already inactive.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the request failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Indicates that not enough memory is available to load the device.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMUS_E_SYNTHNOTCONFIGURED</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the synth is not opened or not properly configured.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMUS_E_NOSYNTHSINK</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the <b>IDirectMusicSynthSink</b> object was not connected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMUS_E_SYNTHACTIVE</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the synth is already active.

</td>
</tr>
</table>

## -remarks

By enabling or disabling the audio device under program control, <code>Activate</code> gives the application the ability to manage its use of resources. When not playing music, the application can deactivate the wave-output resource, which frees it for other applications to use.

The wave-output resource is actually managed by a separate COM object, which has a <a href="/windows/desktop/api/dmusics/nn-dmusics-idirectmusicsynthsink">IDirectMusicSynthSink</a> interface. This object must first be connected with a call to <b>SetSynthSink</b>. Otherwise, the synthesizer will fail the <code>Activate</code> call with DMUS_E_NOSYNTHSINK.

Activation is mostly managed by the wave sink object. When <code>IDirectMusicSynth::Activate</code> is called, the synth sets its internal activation state and calls <a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynthsink-activate">IDirectMusicSynthSink::Activate</a> to enable or disable the wave output.

## -see-also

<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-open">IDirectMusicSynth::Open</a>



<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynthsink-activate">IDirectMusicSynthSink::Activate</a>
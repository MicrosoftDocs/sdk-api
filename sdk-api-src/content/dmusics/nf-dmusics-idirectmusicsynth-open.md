---
UID: NF:dmusics.IDirectMusicSynth.Open
title: IDirectMusicSynth::Open (dmusics.h)
description: The Open method opens a DirectMusic synthesizer &quot;port&quot;.
helpviewer_keywords: ["IDirectMusicSynth interface [Audio Devices]","Open method","IDirectMusicSynth.Open","IDirectMusicSynth::Open","Open","Open method [Audio Devices]","Open method [Audio Devices]","IDirectMusicSynth interface","audio.idirectmusicsynth_open","audmp-routines_5bb9c701-4377-42fb-91ac-733952708a38.xml","dmusics/IDirectMusicSynth::Open"]
old-location: audio\idirectmusicsynth_open.htm
tech.root: dshow
ms.assetid: 15a16b27-7693-4fc6-80ae-e8aedcf879d0
ms.date: 12/05/2018
ms.keywords: IDirectMusicSynth interface [Audio Devices],Open method, IDirectMusicSynth.Open, IDirectMusicSynth::Open, Open, Open method [Audio Devices], Open method [Audio Devices],IDirectMusicSynth interface, audio.idirectmusicsynth_open, audmp-routines_5bb9c701-4377-42fb-91ac-733952708a38.xml, dmusics/IDirectMusicSynth::Open
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
 - IDirectMusicSynth::Open
 - dmusics/IDirectMusicSynth::Open
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
 - IDirectMusicSynth.Open
archived: true
---

# IDirectMusicSynth::Open


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

The port is valid until it is closed by the <a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-close">IDirectMusicSynth::Close</a> method.

When opening the port, some of the parameters asked for in DMUS_PORTPARAMS might not be supported or the port might "upgrade" a parameter request (that is, return the maximum number of voices supported instead of just what was asked for). In either of these cases, the Microsoft Software Synthesizer will return S_FALSE and modify DMUS_PORTPARAMS accordingly, to show what is actually supported. Custom synths should emulate this behavior to ensure compatibility with existing code.

Opening a port is not enough to enable the synthesizer. The synthesizer is enabled by opening the port and enabling audio output through <a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-activate">IDirectMusicSynth::Activate</a>.

Avoid confusing the term DirectMusic "port" with a DMus port driver. A DirectMusic port corresponds to a render or capture pin on a DirectMusic filter. For more information about DirectMusic ports, see the description of the <b>IDirectMusicPort</b> interface in the Windows SDK documentation.

## -see-also

<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-activate">IDirectMusicSynth::Activate</a>



<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-close">IDirectMusicSynth::Close</a>



<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-download">IDirectMusicSynth::Download</a>



<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-playbuffer">IDirectMusicSynth::PlayBuffer</a>



<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-unload">IDirectMusicSynth::Unload</a>



<a href="/windows/desktop/api/dmusics/nn-dmusics-idirectmusicsynthsink">IDirectMusicSynthSink</a>
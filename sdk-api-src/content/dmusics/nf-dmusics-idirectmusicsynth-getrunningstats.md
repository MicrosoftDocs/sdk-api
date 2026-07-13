---
UID: NF:dmusics.IDirectMusicSynth.GetRunningStats
title: IDirectMusicSynth::GetRunningStats (dmusics.h)
description: The GetRunningStats method retrieves current information about the state of the synthesizer so that an application can tell how the synth is performing.
helpviewer_keywords: ["GetRunningStats","GetRunningStats method [Audio Devices]","GetRunningStats method [Audio Devices]","IDirectMusicSynth interface","IDirectMusicSynth interface [Audio Devices]","GetRunningStats method","IDirectMusicSynth.GetRunningStats","IDirectMusicSynth::GetRunningStats","audio.idirectmusicsynth_getrunningstats","audmp-routines_9669d460-7c3b-4769-bb3e-fdca1d347f07.xml","dmusics/IDirectMusicSynth::GetRunningStats"]
old-location: audio\idirectmusicsynth_getrunningstats.htm
tech.root: dshow
ms.assetid: cf3e97f2-6068-4438-b4c7-5e55ba22bd6e
ms.date: 12/05/2018
ms.keywords: GetRunningStats, GetRunningStats method [Audio Devices], GetRunningStats method [Audio Devices],IDirectMusicSynth interface, IDirectMusicSynth interface [Audio Devices],GetRunningStats method, IDirectMusicSynth.GetRunningStats, IDirectMusicSynth::GetRunningStats, audio.idirectmusicsynth_getrunningstats, audmp-routines_9669d460-7c3b-4769-bb3e-fdca1d347f07.xml, dmusics/IDirectMusicSynth::GetRunningStats
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
 - IDirectMusicSynth::GetRunningStats
 - dmusics/IDirectMusicSynth::GetRunningStats
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
 - IDirectMusicSynth.GetRunningStats
archived: true
---

# IDirectMusicSynth::GetRunningStats


## -description

The <code>GetRunningStats</code> method retrieves current information about the state of the synthesizer so that an application can tell how the synth is performing.

## -parameters

### -param pStats

Pointer to a DMUS_SYNTHSTATS structure (described in Microsoft Windows SDK documentation). The method writes the synth's statistics into this structure.

## -returns

<code>GetRunningStats</code> returns S_OK if the call was successful. Otherwise, the method returns an appropriate error code. The following table shows some of the possible return status codes.

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
Indicates that the method is unable to get the stats.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Indicates a bad <i>pStats</i> pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the synthesizer has not implemented this method (so expect the worst!).

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
</table>

## -remarks

The <code>GetRunningStats</code> method returns current information about the state of the synthesizer, including CPU loading, peak volume, and how many notes were stolen (from changing priority levels; see <a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-setchannelpriority">IDirectMusicSynth::SetChannelPriority</a>). The method outputs these statistics into a DMUS_SYNTHSTATS structure.

An application can call <code>GetRunningStats</code> periodically to get the status of the synthesizer as it runs. All of the running status parameters, with the exception of <i>dwFreeMemory</i>, are refreshed every second.

An application typically accesses <code>GetRunningStats</code> indirectly by calling <b>IDirectMusicPort::GetRunningStats</b>, which is described in the Windows SDK documentation.

## -see-also

<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-setchannelpriority">IDirectMusicSynth::SetChannelPriority</a>
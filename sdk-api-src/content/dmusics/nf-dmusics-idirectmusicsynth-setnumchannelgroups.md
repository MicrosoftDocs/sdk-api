---
UID: NF:dmusics.IDirectMusicSynth.SetNumChannelGroups
title: IDirectMusicSynth::SetNumChannelGroups (dmusics.h)
description: The SetNumChannelGroups method instructs the synthesizer to set its number of channel groups to a new value.
helpviewer_keywords: ["IDirectMusicSynth interface [Audio Devices]","SetNumChannelGroups method","IDirectMusicSynth.SetNumChannelGroups","IDirectMusicSynth::SetNumChannelGroups","SetNumChannelGroups","SetNumChannelGroups method [Audio Devices]","SetNumChannelGroups method [Audio Devices]","IDirectMusicSynth interface","audio.idirectmusicsynth_setnumchannelgroups","audmp-routines_7a3156c4-8bab-4ad5-aca6-369f322e6cb7.xml","dmusics/IDirectMusicSynth::SetNumChannelGroups"]
old-location: audio\idirectmusicsynth_setnumchannelgroups.htm
tech.root: dshow
ms.assetid: b7a26fc6-11a9-4bb6-944f-dfbc772b4383
ms.date: 12/05/2018
ms.keywords: IDirectMusicSynth interface [Audio Devices],SetNumChannelGroups method, IDirectMusicSynth.SetNumChannelGroups, IDirectMusicSynth::SetNumChannelGroups, SetNumChannelGroups, SetNumChannelGroups method [Audio Devices], SetNumChannelGroups method [Audio Devices],IDirectMusicSynth interface, audio.idirectmusicsynth_setnumchannelgroups, audmp-routines_7a3156c4-8bab-4ad5-aca6-369f322e6cb7.xml, dmusics/IDirectMusicSynth::SetNumChannelGroups
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
 - IDirectMusicSynth::SetNumChannelGroups
 - dmusics/IDirectMusicSynth::SetNumChannelGroups
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
 - IDirectMusicSynth.SetNumChannelGroups
archived: true
---

# IDirectMusicSynth::SetNumChannelGroups


## -description

The <code>SetNumChannelGroups</code> method instructs the synthesizer to set its number of channel groups to a new value.

## -parameters

### -param dwGroups

Specifies the number of channel groups requested.

## -returns

<code>SetNumChannelGroups</code> returns S_OK if the call was successful. Otherwise, the method returns an appropriate error code. The following table shows some of the possible return status codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the method is unable to allocate the channel groups.

</td>
</tr>
</table>

## -remarks

Even though <a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-open">IDirectMusicSynth::Open</a> tells the DirectMusic "port" how many channel groups to create, the application might later need to dynamically increase or reduce that number with a call to <code>SetNumChannelGroups</code>.

Each channel group supports a set of 16 MIDI channels. For example, if <i>dwChannelGroups</i> is set to three, the synthesizer creates 48 channels.

For more information, see the description of the <b>IDirectMusic</b> interface in the Microsoft Windows SDK documentation.

## -see-also

<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-open">IDirectMusicSynth::Open</a>
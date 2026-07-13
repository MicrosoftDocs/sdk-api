---
UID: NF:dmusics.IDirectMusicSynth.SetChannelPriority
title: IDirectMusicSynth::SetChannelPriority (dmusics.h)
description: The SetChannelPriority method sets the priority of a MIDI channel.
helpviewer_keywords: ["IDirectMusicSynth interface [Audio Devices]","SetChannelPriority method","IDirectMusicSynth.SetChannelPriority","IDirectMusicSynth::SetChannelPriority","SetChannelPriority","SetChannelPriority method [Audio Devices]","SetChannelPriority method [Audio Devices]","IDirectMusicSynth interface","audio.idirectmusicsynth_setchannelpriority","audmp-routines_58d1ca8b-8fc8-4183-a9fa-4b21f11ae86e.xml","dmusics/IDirectMusicSynth::SetChannelPriority"]
old-location: audio\idirectmusicsynth_setchannelpriority.htm
tech.root: dshow
ms.assetid: 6398f460-4c2e-4995-a606-e95e0488f1cd
ms.date: 12/05/2018
ms.keywords: IDirectMusicSynth interface [Audio Devices],SetChannelPriority method, IDirectMusicSynth.SetChannelPriority, IDirectMusicSynth::SetChannelPriority, SetChannelPriority, SetChannelPriority method [Audio Devices], SetChannelPriority method [Audio Devices],IDirectMusicSynth interface, audio.idirectmusicsynth_setchannelpriority, audmp-routines_58d1ca8b-8fc8-4183-a9fa-4b21f11ae86e.xml, dmusics/IDirectMusicSynth::SetChannelPriority
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
 - IDirectMusicSynth::SetChannelPriority
 - dmusics/IDirectMusicSynth::SetChannelPriority
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
 - IDirectMusicSynth.SetChannelPriority
archived: true
---

# IDirectMusicSynth::SetChannelPriority


## -description

The <code>SetChannelPriority</code> method sets the priority of a MIDI channel.

## -parameters

### -param dwChannelGroup

Specifies the group the channel is in. This value must be one or greater.

### -param dwChannel

Specifies a channel in the channel group. This parameter is an index in the range 0 to 15.

### -param dwPriority

Specifies the priority ranking of the channel. For a list of the ranking values that are defined for this parameter, see the <b>IDirectMusicPort::GetChannelPriority</b> reference page in the Microsoft Windows SDK documentation.

## -returns

<code>SetChannelPriority</code> returns S_OK if the call was successful. Otherwise, the method returns an appropriate error code.

## -remarks

The <code>SetChannelPriority</code> method is implemented to support the MIDI synthesis engine. This method allows the allocated voices to run at different priorities, depending on which channel they are on. Sometimes voices are freed when there are too many to deal with at one time, and they are kicked out based on the priority of the channel they are on. If a voice comes in on a higher-priority channel, and if there are no more free voices, the MIDI synthesis engine will steal a channel from the lowest-priority voice and reassign the channels.

For more information, see the description of the <b>IDirectMusicPort::GetChannelPriority</b> and <b>IDirectMusicPort::SetChannelPriority</b> methods in the Windows SDK documentation.

## -see-also

<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-getchannelpriority">IDirectMusicSynth::GetChannelPriority</a>
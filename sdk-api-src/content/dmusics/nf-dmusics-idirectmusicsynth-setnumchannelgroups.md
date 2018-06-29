---
UID: NF:dmusics.IDirectMusicSynth.SetNumChannelGroups
title: IDirectMusicSynth::SetNumChannelGroups
author: windows-sdk-content
description: The SetNumChannelGroups method instructs the synthesizer to set its number of channel groups to a new value.
old-location: audio\idirectmusicsynth_setnumchannelgroups.htm
old-project: audio
ms.assetid: b7a26fc6-11a9-4bb6-944f-dfbc772b4383
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: IDirectMusicSynth interface [Audio Devices],SetNumChannelGroups method, IDirectMusicSynth.SetNumChannelGroups, IDirectMusicSynth::SetNumChannelGroups, SetNumChannelGroups, SetNumChannelGroups method [Audio Devices], SetNumChannelGroups method [Audio Devices],IDirectMusicSynth interface, audio.idirectmusicsynth_setnumchannelgroups, audmp-routines_7a3156c4-8bab-4ad5-aca6-369f322e6cb7.xml, dmusics/IDirectMusicSynth::SetNumChannelGroups
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DMO_PARTIAL_MEDIATYPE, *PDMO_PARTIAL_MEDIATYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dmusics.h
api_name:
 - IDirectMusicSynth.SetNumChannelGroups
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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



Even though <a href="https://msdn.microsoft.com/library/windows/hardware/ff536539">IDirectMusicSynth::Open</a> tells the DirectMusic "port" how many channel groups to create, the application might later need to dynamically increase or reduce that number with a call to <code>SetNumChannelGroups</code>.

Each channel group supports a set of 16 MIDI channels. For example, if <i>dwChannelGroups</i> is set to three, the synthesizer creates 48 channels.

For more information, see the description of the <b>IDirectMusic</b> interface in the Microsoft Windows SDK documentation.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff536539">IDirectMusicSynth::Open</a>
 

 


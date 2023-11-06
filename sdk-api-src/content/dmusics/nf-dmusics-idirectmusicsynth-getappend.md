---
UID: NF:dmusics.IDirectMusicSynth.GetAppend
title: IDirectMusicSynth::GetAppend (dmusics.h)
description: The GetAppend method outputs the number of additional wave samples that the DirectMusic &quot;port&quot; needs to have appended to the end of a download buffer.
helpviewer_keywords: ["GetAppend","GetAppend method [Audio Devices]","GetAppend method [Audio Devices]","IDirectMusicSynth interface","IDirectMusicSynth interface [Audio Devices]","GetAppend method","IDirectMusicSynth.GetAppend","IDirectMusicSynth::GetAppend","audio.idirectmusicsynth_getappend","audmp-routines_691b2730-4c18-43c7-b5cd-1ee1f94c5e3d.xml","dmusics/IDirectMusicSynth::GetAppend"]
old-location: audio\idirectmusicsynth_getappend.htm
tech.root: dshow
ms.assetid: fc250e51-2e7d-4406-a8cf-7b7430a0ef7c
ms.date: 12/05/2018
ms.keywords: GetAppend, GetAppend method [Audio Devices], GetAppend method [Audio Devices],IDirectMusicSynth interface, IDirectMusicSynth interface [Audio Devices],GetAppend method, IDirectMusicSynth.GetAppend, IDirectMusicSynth::GetAppend, audio.idirectmusicsynth_getappend, audmp-routines_691b2730-4c18-43c7-b5cd-1ee1f94c5e3d.xml, dmusics/IDirectMusicSynth::GetAppend
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
 - IDirectMusicSynth::GetAppend
 - dmusics/IDirectMusicSynth::GetAppend
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
 - IDirectMusicSynth.GetAppend
archived: true
---

# IDirectMusicSynth::GetAppend


## -description

The <code>GetAppend</code> method outputs the number of additional wave samples that the DirectMusic "port" needs to have appended to the end of a download buffer.

## -parameters

### -param pdwAppend

Output pointer for the number of samples to append. This parameter points to a caller-allocated variable into which the method writes a count specifying the number of appended samples for which memory is required. The required memory in bytes can be calculated from the wave format.

## -returns

<code>GetAppend</code> returns S_OK if the call was successful. Otherwise, the method returns an appropriate error code. The following table shows some of the possible return status codes.

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
Indicates that the pointer buffer is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the method is not implemented.

</td>
</tr>
</table>

## -remarks

This method is called to determine how much extra storage to provide at the end of a download buffer. The method outputs a count indicating the number of additional wave samples by which the buffer should be extended.

When downloading a waveform, the synth might need to attach a little more data at the end of the waveform, depending on how the synth is implemented. The port's synthesis engine can use this extra memory to interpolate across a loop boundary.

For example, if a wave loops for 20 samples at the end, the interpolation math that calculates what to do as it loops back might require some extra data at the end so that it can interpolate properly.

Extending the download buffer by the <i>pdwAppend</i> amount allows the synth to simply add the extra samples to the end of the buffer. Otherwise, the synth would have to copy the contents of the download buffer to a larger buffer in order to have room to append the extra data.

Avoid confusing the term DirectMusic "port" with a DMus port driver. A DirectMusic port corresponds to a render or capture pin on a DirectMusic filter. For more information about DirectMusic ports, see the description of the <b>IDirectMusicPort</b> interface in the Microsoft Windows SDK documentation.


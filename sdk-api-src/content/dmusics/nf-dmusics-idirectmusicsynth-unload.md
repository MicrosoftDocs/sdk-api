---
UID: NF:dmusics.IDirectMusicSynth.Unload
title: IDirectMusicSynth::Unload (dmusics.h)
description: The Unload method unloads a DLS resource (waveform or articulation data for a MIDI instrument) that was previously downloaded by a call to IDirectMusicSynth::Download.
helpviewer_keywords: ["IDirectMusicSynth interface [Audio Devices]","Unload method","IDirectMusicSynth.Unload","IDirectMusicSynth::Unload","Unload","Unload method [Audio Devices]","Unload method [Audio Devices]","IDirectMusicSynth interface","audio.idirectmusicsynth_unload","audmp-routines_7a0213c4-3cd1-4c6f-ab4a-064d08782629.xml","dmusics/IDirectMusicSynth::Unload"]
old-location: audio\idirectmusicsynth_unload.htm
tech.root: dshow
ms.assetid: 608ebffe-873a-40ed-a411-245e8b6ceabd
ms.date: 12/05/2018
ms.keywords: IDirectMusicSynth interface [Audio Devices],Unload method, IDirectMusicSynth.Unload, IDirectMusicSynth::Unload, Unload, Unload method [Audio Devices], Unload method [Audio Devices],IDirectMusicSynth interface, audio.idirectmusicsynth_unload, audmp-routines_7a0213c4-3cd1-4c6f-ab4a-064d08782629.xml, dmusics/IDirectMusicSynth::Unload
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
 - IDirectMusicSynth::Unload
 - dmusics/IDirectMusicSynth::Unload
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
 - IDirectMusicSynth.Unload
archived: true
---

# IDirectMusicSynth::Unload


## -description

The <code>Unload</code> method unloads a DLS resource (waveform or articulation data for a MIDI instrument) that was previously downloaded by a call to <a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-download">IDirectMusicSynth::Download</a>.

## -parameters

### -param hDownload

Handle to the DLS resource, which was obtained from a previous call to the <b>IDirectMusicSynth::Download</b> method. If the <i>lpFreeHandle</i> parameter below is non-<b>NULL</b>, the synthesizer passes this handle as the first parameter to the <i>lpFreeHandle</i> callback routine.

### -param lpFreeHandle

Pointer to a callback routine that will be called when the memory containing the DLS resource is no longer in use. If the original call to <b>IDirectMusicSynth::Download</b> returned <b>FALSE</b> in <i>pbFree</i>, this means that the synthesizer continued accessing the caller-allocated memory in the download chunk after the return from <b>Download</b>. If so, the synthesizer notifies the caller as soon as the memory can be freed, but this might occur later than the return from <code>Unload</code> because the DLS resource might be currently in use. The callback function takes two handles as call parameters. The first of these two handles is the <i>hDownload</i> parameter (see above), and the second is the <i>hUserData</i> parameter (see below).

### -param hUserData

Pointer to user data, which is passed as the second parameter to the <i>lpFreeHandle</i> callback function above. The meaning of this value is known only to the caller, but it is typically a pointer to context information describing the state of the memory that is to be freed.

## -returns

<code>Unload</code> returns S_OK if the call was successful. Otherwise, the method returns an appropriate error code. The following table shows some of the possible return status codes.

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
Indicates that the method is unable to unload data (<i>hDownload</i> probably invalid).

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

When the caller downloads a DLS resource to the synthesizer by calling <b>IDirectMusicSynth::Download</b>, the synthesizer has the option of either making its own copy of the DLS resource or continuing to use the caller's copy of the DLS resource. The <b>Download</b> method specifies one of these options by the value that it outputs through its <i>pbFree</i> parameter:

<ul>
<li>
*<i>pbFree</i>=<b>TRUE</b> if the synthesizer makes its own copy. In this case, the caller can free the DLS memory on return from <b>Download</b>. Also, the caller can specify the values for the <code>Unload</code> method's <i>lpFreeHandle</i> and <i>hUserData</i> parameters as <b>NULL</b>.

</li>
<li>
*<i>pbFree</i>=<b>FALSE</b> if the synthesizer keeps a pointer to the caller's copy. In this case, the caller must maintain its allocation of the memory containing the DLS resource until the synthesizer has finished using that memory.

</li>
</ul>
In the latter case, the caller must not release the memory for the DLS resource immediately on return from the <code>Unload</code> call because the synthesizer might still be in the process of rendering a note that uses the DLS resource. Instead, the caller must wait for the synthesizer to call the <i>lpFreeHandle</i> callback routine, which the synthesizer will do as soon as the note finishes and the memory is no longer needed.

For more information, see the descriptions of the <b>IDirectMusic</b> and <b>IDirectMusicPort</b> interfaces and the <b>IDirectMusicPort::UnloadInstrument</b> method in the Microsoft Windows SDK documentation.

## -see-also

<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-download">IDirectMusicSynth::Download</a>
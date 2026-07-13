---
UID: NF:dmusics.IDirectMusicSynth.Close
title: IDirectMusicSynth::Close (dmusics.h)
description: The Close method closes a DirectMusic &quot;port&quot;, which is a DirectMusic term for a device that sends or receives music data.
helpviewer_keywords: ["Close","Close method [Audio Devices]","Close method [Audio Devices]","IDirectMusicSynth interface","IDirectMusicSynth interface [Audio Devices]","Close method","IDirectMusicSynth.Close","IDirectMusicSynth::Close","audio.idirectmusicsynth_close","audmp-routines_e0ff55d1-46e2-42a0-afe4-a4129e663ddd.xml","dmusics/IDirectMusicSynth::Close"]
old-location: audio\idirectmusicsynth_close.htm
tech.root: dshow
ms.assetid: 275d9ad3-9dde-4cfb-a67f-24da3a0ad2ce
ms.date: 12/05/2018
ms.keywords: Close, Close method [Audio Devices], Close method [Audio Devices],IDirectMusicSynth interface, IDirectMusicSynth interface [Audio Devices],Close method, IDirectMusicSynth.Close, IDirectMusicSynth::Close, audio.idirectmusicsynth_close, audmp-routines_e0ff55d1-46e2-42a0-afe4-a4129e663ddd.xml, dmusics/IDirectMusicSynth::Close
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
 - IDirectMusicSynth::Close
 - dmusics/IDirectMusicSynth::Close
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
 - IDirectMusicSynth.Close
---

## -description

The <code>Close</code> method closes a DirectMusic "port", which is a DirectMusic term for a device that sends or receives music data.



## -returns

<code>Close</code> returns S_OK if the call was successful. Otherwise, the method returns an appropriate error code. The following table shows some of the possible return status codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMUS_E_ALREADYCLOSED</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the port was not open.

</td>
</tr>
</table>

## -remarks

This method closes a DirectMusic "port" that was previously opened by a call to <a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-open">IDirectMusicSynth::Open</a>.

When the DirectMusic "port" closes, it automatically releases all instruments and waves that were previously downloaded to the port. However, a good practice for applications is to explicitly free these objects before closing the port.

Avoid confusing the term DirectMusic "port" with a DMus port driver. A DirectMusic port corresponds to a render or capture pin on a DirectMusic filter. For more information about DirectMusic ports, see the description of the <b>IDirectMusicPort</b> interface in the Microsoft Windows SDK documentation.

## -see-also

<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-open">IDirectMusicSynth::Open</a>

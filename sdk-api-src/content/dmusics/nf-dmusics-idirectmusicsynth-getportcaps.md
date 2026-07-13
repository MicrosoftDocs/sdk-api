---
UID: NF:dmusics.IDirectMusicSynth.GetPortCaps
title: IDirectMusicSynth::GetPortCaps (dmusics.h)
description: The GetPortCaps method retrieves the capabilities of a DirectMusic &quot;port&quot;, which is a DirectMusic term for a device that sends or receives music data.
helpviewer_keywords: ["GetPortCaps","GetPortCaps method [Audio Devices]","GetPortCaps method [Audio Devices]","IDirectMusicSynth interface","IDirectMusicSynth interface [Audio Devices]","GetPortCaps method","IDirectMusicSynth.GetPortCaps","IDirectMusicSynth::GetPortCaps","audio.idirectmusicsynth_getportcaps","audmp-routines_b2b05c43-5c58-414c-aac4-3a37eceab293.xml","dmusics/IDirectMusicSynth::GetPortCaps"]
old-location: audio\idirectmusicsynth_getportcaps.htm
tech.root: dshow
ms.assetid: 9e4ba4e3-5bd7-4a90-a591-8bffaa0265d0
ms.date: 12/05/2018
ms.keywords: GetPortCaps, GetPortCaps method [Audio Devices], GetPortCaps method [Audio Devices],IDirectMusicSynth interface, IDirectMusicSynth interface [Audio Devices],GetPortCaps method, IDirectMusicSynth.GetPortCaps, IDirectMusicSynth::GetPortCaps, audio.idirectmusicsynth_getportcaps, audmp-routines_b2b05c43-5c58-414c-aac4-3a37eceab293.xml, dmusics/IDirectMusicSynth::GetPortCaps
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
 - IDirectMusicSynth::GetPortCaps
 - dmusics/IDirectMusicSynth::GetPortCaps
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
 - IDirectMusicSynth.GetPortCaps
archived: true
---

# IDirectMusicSynth::GetPortCaps


## -description

The <code>GetPortCaps</code> method retrieves the capabilities of a DirectMusic "port", which is a DirectMusic term for a device that sends or receives music data.

## -parameters

### -param pCaps

Pointer to a DMUS_PORTCAPS structure (described in the Microsoft Windows SDK documentation). The method writes the capabilities of the DirectMusic "port" into this structure.

## -returns

<code>GetPortCaps</code> returns S_OK if the call was successful. Otherwise, the method returns an appropriate error code. The following table shows some of the possible return status codes.

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
Indicates a bad <i>pCaps</i> pointer.

</td>
</tr>
</table>

## -remarks

When an application enumerates the available DirectMusic "ports" with a call to <b>IDirectMusic::EnumPort</b> (described in the Windows SDK documentation), DirectMusic calls each registered device's <code>GetPortCaps</code> method.

This means that the additional overhead of creating and initializing the synthesizer occurs with this call. It is a good idea to keep the overhead of simply creating a synthesizer to a minimum, because there is a chance that it is being created only so that its capabilities can be obtained, and then it will be released.

Avoid confusing the term DirectMusic "port" with a DMus port driver. A DirectMusic port corresponds to a render or capture pin on a DirectMusic filter. For more information about DirectMusic ports, see the description of the <b>IDirectMusicPort</b> interface in the Windows SDK documentation.


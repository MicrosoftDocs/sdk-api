---
UID: NF:mmeapi.midiOutCachePatches
title: midiOutCachePatches function (mmeapi.h)
description: The midiOutCachePatches function requests that an internal MIDI synthesizer device preload and cache a specified set of patches.
helpviewer_keywords: ["_win32_midiOutCachePatches","midiOutCachePatches","midiOutCachePatches function [Windows Multimedia]","mmeapi/midiOutCachePatches","multimedia.midioutcachepatches"]
old-location: multimedia\midioutcachepatches.htm
tech.root: Multimedia
ms.assetid: 58d0c73b-46a4-498d-bcef-f5b8aaf52392
ms.date: 12/05/2018
ms.keywords: _win32_midiOutCachePatches, midiOutCachePatches, midiOutCachePatches function [Windows Multimedia], mmeapi/midiOutCachePatches, multimedia.midioutcachepatches
req.header: mmeapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Winmm.lib
req.dll: Winmm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - midiOutCachePatches
 - mmeapi/midiOutCachePatches
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winmm.dll
 - API-MS-Win-mm-mme-l1-1-0.dll
 - winmmbase.dll
api_name:
 - midiOutCachePatches
---

# midiOutCachePatches function


## -description

The <b>midiOutCachePatches</b> function requests that an internal MIDI synthesizer device preload and cache a specified set of patches.

## -parameters

### -param hmo

Handle to the opened MIDI output device. This device must be an internal MIDI synthesizer. This parameter can also be the handle of a MIDI stream, cast to <b>HMIDIOUT</b>.

### -param uBank

Bank of patches that should be used. This parameter should be set to zero to cache the default patch bank.

### -param pwpa

Pointer to a <a href="/windows/desktop/Multimedia/patcharray">PATCHARRAY</a> array indicating the patches to be cached or uncached.

### -param fuCache

Options for the cache operation. It can be one of the following flags.

<table>
<tr>
<th>Value
</th>
<th>Meaning
</th>
</tr>
<tr>
<td>MIDI_CACHE_ALL</td>
<td>Caches all of the specified patches. If they cannot all be cached, it caches none, clears the <a href="/windows/desktop/Multimedia/patcharray">PATCHARRAY</a> array, and returns MMSYSERR_NOMEM.</td>
</tr>
<tr>
<td>MIDI_CACHE_BESTFIT</td>
<td>Caches all of the specified patches. If they cannot all be cached, it caches as many patches as possible, changes the PATCHARRAY array to reflect which patches were cached, and returns MMSYSERR_NOMEM.</td>
</tr>
<tr>
<td>MIDI_CACHE_QUERY</td>
<td>Changes the <a href="/windows/desktop/Multimedia/patcharray">PATCHARRAY</a> array to indicate which patches are currently cached.</td>
</tr>
<tr>
<td>MIDI_UNCACHE</td>
<td>Uncaches the specified patches and clears the PATCHARRAY array.</td>
</tr>
</table>

## -returns

Returns MMSYSERR_NOERROR if successful or an error otherwise. Possible error values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_INVALFLAG</b></dt>
</dl>
</td>
<td width="60%">
The flag specified by <i>wFlags</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_INVALHANDLE</b></dt>
</dl>
</td>
<td width="60%">
The specified device handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_INVALPARAM</b></dt>
</dl>
</td>
<td width="60%">
The array pointed to by <i>lpPatchArray</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_NOMEM</b></dt>
</dl>
</td>
<td width="60%">
The device does not have enough memory to cache all of the requested patches.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_NOTSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The specified device does not support patch caching.

</td>
</tr>
</table>

## -remarks

Some synthesizers are not capable of keeping all patches loaded simultaneously and must load data from disk when they receive MIDI program change messages. Caching patches ensures that the specified patches are immediately available.

Each element of the <a href="/windows/desktop/Multimedia/patcharray">PATCHARRAY</a> array represents one of the 128 patches and has bits set for each of the 16 MIDI channels that use the particular patch. The least-significant bit represents physical channel 0, and the most-significant bit represents physical channel 15 (0x0F). For example, if patch 0 is used by physical channels 0 and 8, element 0 would be set to 0x0101.

This function applies only to internal MIDI synthesizer devices. Not all internal synthesizers support patch caching. To see if a device supports patch caching, use the MIDICAPS_CACHE flag to test the <b>dwSupport</b> member of the <a href="/previous-versions/dd798467(v=vs.85)">MIDIOUTCAPS</a> structure filled by the <a href="/previous-versions/dd798469(v=vs.85)">midiOutGetDevCaps</a> function.

## -see-also

<a href="/windows/desktop/Multimedia/midi-functions">MIDI Functions</a>
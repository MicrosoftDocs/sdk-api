---
UID: NF:mmeapi.midiOutCacheDrumPatches
title: midiOutCacheDrumPatches function (mmeapi.h)
author: windows-sdk-content
description: The midiOutCacheDrumPatches function requests that an internal MIDI synthesizer device preload and cache a specified set of key-based percussion patches.
old-location: multimedia\midioutcachedrumpatches.htm
tech.root: Multimedia
ms.assetid: 2cd5d6d9-7bff-40f9-a088-d66e06ca147c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "_win32_midiOutCacheDrumPatches, midiOutCacheDrumPatches, midiOutCacheDrumPatches function [Windows Multimedia], midiOutCacheDrumPatchesA, midiOutCacheDrumPatchesW, mmeapi/midiOutCacheDrumPatches, multimedia.midioutcachedrumpatches"
ms.topic: function
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
 - midiOutCacheDrumPatches
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# midiOutCacheDrumPatches function


## -description



The <b>midiOutCacheDrumPatches</b> function requests that an internal MIDI synthesizer device preload and cache a specified set of key-based percussion patches.




## -parameters




### -param hmo

Handle to the opened MIDI output device. This device should be an internal MIDI synthesizer. This parameter can also be the handle of a MIDI stream, cast to <b>HMIDIOUT</b>.


### -param uPatch

Drum patch number that should be used. This parameter should be set to zero to cache the default drum patch.


### -param pwkya

Pointer to a <a href="https://msdn.microsoft.com/af1a1d2f-4558-4374-93ab-5a705fc879ca">KEYARRAY</a> array indicating the key numbers of the specified percussion patches to be cached or uncached.


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
<td>Caches all of the specified patches. If they cannot all be cached, it caches none, clears the <a href="https://msdn.microsoft.com/af1a1d2f-4558-4374-93ab-5a705fc879ca">KEYARRAY</a> array, and returns MMSYSERR_NOMEM.</td>
</tr>
<tr>
<td>MIDI_CACHE_BESTFIT</td>
<td>Caches all of the specified patches. If they cannot all be cached, it caches as many patches as possible, changes the KEYARRAY array to reflect which patches were cached, and returns MMSYSERR_NOMEM.</td>
</tr>
<tr>
<td>MIDI_CACHE_QUERY</td>
<td>Changes the <a href="https://msdn.microsoft.com/af1a1d2f-4558-4374-93ab-5a705fc879ca">KEYARRAY</a> array to indicate which patches are currently cached.</td>
</tr>
<tr>
<td>MIDI_UNCACHE</td>
<td>Uncaches the specified patches and clears the KEYARRAY array.</td>
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
The array pointed to by the <i>lpKeyArray</i> array is invalid.

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



Some synthesizers are not capable of keeping all percussion patches loaded simultaneously. Caching patches ensures that the specified patches are available.

Each element of the <a href="https://msdn.microsoft.com/af1a1d2f-4558-4374-93ab-5a705fc879ca">KEYARRAY</a> array represents one of the 128 key-based percussion patches and has bits set for each of the 16 MIDI channels that use the particular patch. The least-significant bit represents physical channel 0, and the most-significant bit represents physical channel 15. For example, if the patch on key number 60 is used by physical channels 9 and 15, element 60 would be set to 0x8200.

This function applies only to internal MIDI synthesizer devices. Not all internal synthesizers support patch caching. To see if a device supports patch caching, use the MIDICAPS_CACHE flag to test the <b>dwSupport</b> member of the <a href="https://msdn.microsoft.com/395d5fc2-cf34-48f0-a0b0-185247309e2c">MIDIOUTCAPS</a> structure filled by the <a href="https://msdn.microsoft.com/8777a903-fd47-4f3f-b534-1e72a5951846">midiOutGetDevCaps</a> function.




## -see-also




<a href="https://msdn.microsoft.com/9aa9fd79-cd9e-4443-8715-142ea72b82c0">MIDI Functions</a>
 

 


---
UID: NF:mmeapi.midiStreamProperty
title: midiStreamProperty function (mmeapi.h)
description: The midiStreamProperty function sets or retrieves properties of a MIDI data stream associated with a MIDI output device.
helpviewer_keywords: ["_win32_midiStreamProperty","midiStreamProperty","midiStreamProperty function [Windows Multimedia]","mmeapi/midiStreamProperty","multimedia.midistreamproperty"]
old-location: multimedia\midistreamproperty.htm
tech.root: Multimedia
ms.assetid: fb0f8bf4-5802-444e-9b2e-d9a7c80e3a20
ms.date: 12/05/2018
ms.keywords: _win32_midiStreamProperty, midiStreamProperty, midiStreamProperty function [Windows Multimedia], mmeapi/midiStreamProperty, multimedia.midistreamproperty
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
 - midiStreamProperty
 - mmeapi/midiStreamProperty
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
 - midiStreamProperty
---

# midiStreamProperty function


## -description

The <b>midiStreamProperty</b> function sets or retrieves properties of a MIDI data stream associated with a MIDI output device.

## -parameters

### -param hms

Handle to the MIDI device that the property is associated with.

### -param lppropdata

Pointer to the property data.

### -param dwProperty

Flags that specify the action to perform and identify the appropriate property of the MIDI data stream. The <b>midiStreamProperty</b> function requires setting two flags in each use. One flag (either MIDIPROP_GET or MIDIPROP_SET) specifies an action, and the other identifies a specific property to examine or edit.

<table>
<tr>
<th>Value
</th>
<th>Meaning
</th>
</tr>
<tr>
<td>MIDIPROP_GET</td>
<td>Retrieves the current setting of the given property.</td>
</tr>
<tr>
<td>MIDIPROP_SET</td>
<td>Sets the given property.</td>
</tr>
<tr>
<td>MIDIPROP_TEMPO</td>
<td>Retrieves the tempo property. The <i>lppropdata</i> parameter points to a <a href="/previous-versions/dd798483(v=vs.85)">MIDIPROPTEMPO</a> structure. The current tempo value can be retrieved at any time. Output devices set the tempo by inserting MEVT_TEMPO events into the MIDI data.</td>
</tr>
<tr>
<td>MIDIPROP_TIMEDIV</td>
<td>Specifies the time division property. You can get or set this property. The <i>lppropdata</i> parameter points to a <a href="/previous-versions/dd798484(v=vs.85)">MIDIPROPTIMEDIV</a> structure. This property can be set only when the device is stopped.</td>
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
<dt><b>MMSYSERR_INVALHANDLE</b></dt>
</dl>
</td>
<td width="60%">
The specified handle is not a stream handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_INVALPARAM</b></dt>
</dl>
</td>
<td width="60%">
The given handle or flags parameter is invalid.

</td>
</tr>
</table>

## -remarks

These properties are the default properties defined by the system. Driver writers can implement and document their own properties.

## -see-also

<a href="/windows/desktop/Multimedia/midi-functions">MIDI Functions</a>
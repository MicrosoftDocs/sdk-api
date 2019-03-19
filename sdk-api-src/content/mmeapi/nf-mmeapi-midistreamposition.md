---
UID: NF:mmeapi.midiStreamPosition
title: midiStreamPosition function (mmeapi.h)
author: windows-sdk-content
description: The midiStreamPosition function retrieves the current position in a MIDI stream.
old-location: multimedia\midistreamposition.htm
tech.root: Multimedia
ms.assetid: 77d859bb-1f1b-4a95-939e-88bdf31b1959
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "_win32_midiStreamPosition, midiStreamPosition, midiStreamPosition function [Windows Multimedia], mmeapi/midiStreamPosition, multimedia.midistreamposition"
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
 - midiStreamPosition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# midiStreamPosition function


## -description



The <b>midiStreamPosition</b> function retrieves the current position in a MIDI stream.




## -parameters




### -param hms

Handle to a MIDI stream. This handle must have been returned by a call to the <a href="https://msdn.microsoft.com/355cf034-e1d7-4530-b117-4c505ad0aac6">midiStreamOpen</a> function. This handle identifies the output device.


### -param lpmmt

Pointer to an <a href="https://msdn.microsoft.com/94bb7235-2477-4923-add8-f0c8ac8195c2">MMTIME</a> structure.


### -param cbmmt

Size, in bytes, of the <a href="https://msdn.microsoft.com/94bb7235-2477-4923-add8-f0c8ac8195c2">MMTIME</a> structure.


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
Specified device handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_INVALPARAM</b></dt>
</dl>
</td>
<td width="60%">
Specified pointer or structure is invalid.

</td>
</tr>
</table>
 




## -remarks



Before calling <b>midiStreamPosition</b>, set the <b>wType</b> member of the <a href="https://msdn.microsoft.com/94bb7235-2477-4923-add8-f0c8ac8195c2">MMTIME</a> structure to indicate the time format you desire. After calling <b>midiStreamPosition</b>, check the <b>wType</b> member to determine if the desired time format is supported. If the desired format is not supported, <b>wType</b> will specify an alternative format.

The position is set to zero when the device is opened or reset.




## -see-also




<a href="https://msdn.microsoft.com/9aa9fd79-cd9e-4443-8715-142ea72b82c0">MIDI Functions</a>
 

 


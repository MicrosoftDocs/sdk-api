---
UID: NF:mmeapi.midiDisconnect
title: midiDisconnect function
author: windows-sdk-content
description: The midiDisconnect function disconnects a MIDI input device from a MIDI thru or output device, or disconnects a MIDI thru device from a MIDI output device.
old-location: multimedia\mididisconnect.htm
tech.root: Multimedia
ms.assetid: bf6ea7d0-eb0a-429f-8029-d283808fb85e
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "_win32_midiDisconnect, midiDisconnect, midiDisconnect function [Windows Multimedia], mmeapi/midiDisconnect, multimedia.mididisconnect"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - midiDisconnect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# midiDisconnect function


## -description



The <b>midiDisconnect</b> function disconnects a MIDI input device from a MIDI thru or output device, or disconnects a MIDI thru device from a MIDI output device.




## -parameters




### -param hmi

TBD


### -param hmo

Handle to the MIDI output device to be disconnected.


### -param pReserved

Reserved; must be <b>NULL</b>.


#### - hMidi

Handle to a MIDI input device or a MIDI thru device.


## -returns



Returns MMSYSERR_NOERROR if successful or an error otherwise. Possible error values include the following:.

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
</table>
 




## -remarks



MIDI input, output, and thru devices can be connected by using the <b>midiConnect</b> function. Thereafter, whenever the MIDI input device receives event data in an MIM_DATA message, a message with the same event data is sent to the output device driver (or through the thru driver to the output drivers).




## -see-also




<a href="https://msdn.microsoft.com/9aa9fd79-cd9e-4443-8715-142ea72b82c0">MIDI Functions</a>
 

 


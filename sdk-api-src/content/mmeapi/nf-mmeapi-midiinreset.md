---
UID: NF:mmeapi.midiInReset
title: midiInReset function (mmeapi.h)
author: windows-sdk-content
description: The midiInReset function stops input on a given MIDI input device.
old-location: multimedia\midiinreset.htm
tech.root: Multimedia
ms.assetid: 74df14c2-df28-40c0-81f2-aed2147f7072
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "_win32_midiInReset, midiInReset, midiInReset function [Windows Multimedia], mmeapi/midiInReset, multimedia.midiinreset"
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
 - midiInReset
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# midiInReset function


## -description



The <b>midiInReset</b> function stops input on a given MIDI input device.




## -parameters




### -param hmi

Handle to the MIDI input device.


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
The specified device handle is invalid.

</td>
</tr>
</table>
 




## -remarks



This function returns all pending input buffers to the callback function and sets the MHDR_DONE flag in the <b>dwFlags</b> member of the <a href="https://msdn.microsoft.com/630f0645-555e-4f48-9397-2623a9918b8a">MIDIHDR</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/9aa9fd79-cd9e-4443-8715-142ea72b82c0">MIDI Functions</a>
 

 


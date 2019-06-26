---
UID: NF:mmeapi.midiStreamClose
title: midiStreamClose function (mmeapi.h)
author: windows-sdk-content
description: The midiStreamClose function closes an open MIDI stream.
old-location: multimedia\midistreamclose.htm
tech.root: Multimedia
ms.assetid: 53096399-3e79-4534-8b67-ccb70c32ccf0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "_win32_midiStreamClose, midiStreamClose, midiStreamClose function [Windows Multimedia], mmeapi/midiStreamClose, multimedia.midistreamclose"
ms.topic: function
f1_keywords: 
 - "mmeapi/midiStreamClose"
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
 - midiStreamClose
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# midiStreamClose function


## -description



The <b>midiStreamClose</b> function closes an open MIDI stream.




## -parameters




### -param hms

Handle to a MIDI stream, as retrieved by using the <a href="https://docs.microsoft.com/previous-versions/dd798486(v=vs.85)">midiStreamOpen</a> function.


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
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/midi-functions">MIDI Functions</a>
 

 


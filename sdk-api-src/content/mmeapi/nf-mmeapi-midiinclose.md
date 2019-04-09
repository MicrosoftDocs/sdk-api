---
UID: NF:mmeapi.midiInClose
title: midiInClose function (mmeapi.h)
author: windows-sdk-content
description: The midiInClose function closes the specified MIDI input device.
old-location: multimedia\midiinclose.htm
tech.root: Multimedia
ms.assetid: 95a1490c-3a0f-4380-a11f-0979e94f88ab
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "_win32_midiInClose, midiInClose, midiInClose function [Windows Multimedia], mmeapi/midiInClose, multimedia.midiinclose"
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
 - midiInClose
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# midiInClose function


## -description



The <b>midiInClose</b> function closes the specified MIDI input device.




## -parameters




### -param hmi

Handle to the MIDI input device. If the function is successful, the handle is no longer valid after the call to this function.


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
<dt><b>MIDIERR_STILLPLAYING</b></dt>
</dl>
</td>
<td width="60%">
Buffers are still in the queue.

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
<dt><b>MMSYSERR_NOMEM</b></dt>
</dl>
</td>
<td width="60%">
The system is unable to allocate or lock memory.

</td>
</tr>
</table>
 




## -remarks



If there are input buffers that have been sent by using the <a href="https://msdn.microsoft.com/b673e252-91d0-45b9-a528-079868b47157">midiInAddBuffer</a> function and have not been returned to the application, the close operation will fail. To return all pending buffers through the callback function, use the <a href="https://msdn.microsoft.com/74df14c2-df28-40c0-81f2-aed2147f7072">midiInReset</a> function.




## -see-also




<a href="https://msdn.microsoft.com/9aa9fd79-cd9e-4443-8715-142ea72b82c0">MIDI Functions</a>
 

 


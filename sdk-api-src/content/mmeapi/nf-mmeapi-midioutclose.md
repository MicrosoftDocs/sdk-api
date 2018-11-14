---
UID: NF:mmeapi.midiOutClose
title: midiOutClose function
author: windows-sdk-content
description: The midiOutClose function closes the specified MIDI output device.
old-location: multimedia\midioutclose.htm
tech.root: Multimedia
ms.assetid: 4f23295c-1c2c-4060-9c19-b3f0ed5bf44c
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: "_win32_midiOutClose, midiOutClose, midiOutClose function [Windows Multimedia], mmeapi/midiOutClose, multimedia.midioutclose"
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
 - midiOutClose
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- midiOutClose
: 
---

# midiOutClose function


## -description



The <b>midiOutClose</b> function closes the specified MIDI output device.




## -parameters




### -param hmo

Handle to the MIDI output device. If the function is successful, the handle is no longer valid after the call to this function.


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
The system is unable to load mapper string description.

</td>
</tr>
</table>
 




## -remarks



If there are output buffers that have been sent by using the <a href="https://msdn.microsoft.com/7fda802b-eed5-4a27-8bc0-1f43f4722d33">midiOutLongMsg</a> function and have not been returned to the application, the close operation will fail. To mark all pending buffers as being done, use the <a href="https://msdn.microsoft.com/75abf36d-906f-48d1-b91d-c3fcef586693">midiOutReset</a> function.




## -see-also




<a href="https://msdn.microsoft.com/9aa9fd79-cd9e-4443-8715-142ea72b82c0">MIDI Functions</a>
 

 


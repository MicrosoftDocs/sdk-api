---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# MessageBeep function


## -description


Plays a waveform sound. The waveform sound for each sound type is identified by an entry in the 
    registry.


## -parameters




### -param uType [in]

The sound to be played. The sounds are set by the user through the Sound control panel application, and then 
       stored in the registry.

This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
0xFFFFFFFF

</td>
<td>
A simple beep. If the sound card is not available, the sound is generated using the speaker.

</td>
</tr>
<tr>
<td>
<dl>
<dt><b>MB_ICONASTERISK</b></dt>
<dt>0x00000040L</dt>
</dl>
</td>
<td>
See <b>MB_ICONINFORMATION</b>.

</td>
</tr>
<tr>
<td>
<dl>
<dt><b>MB_ICONEXCLAMATION</b></dt>
<dt>0x00000030L</dt>
</dl>
</td>
<td>
See <b>MB_ICONWARNING</b>.

</td>
</tr>
<tr>
<td>
<dl>
<dt><b>MB_ICONERROR</b></dt>
<dt>0x00000010L</dt>
</dl>
</td>
<td>
The sound specified as the Windows Critical Stop sound.

</td>
</tr>
<tr>
<td>
<dl>
<dt><b>MB_ICONHAND</b></dt>
<dt>0x00000010L</dt>
</dl>
</td>
<td>
See <b>MB_ICONERROR</b>.

</td>
</tr>
<tr>
<td>
<dl>
<dt><b>MB_ICONINFORMATION</b></dt>
<dt>0x00000040L</dt>
</dl>
</td>
<td>
The sound specified as the Windows Asterisk sound.

</td>
</tr>
<tr>
<td>
<dl>
<dt><b>MB_ICONQUESTION</b></dt>
<dt>0x00000020L</dt>
</dl>
</td>
<td>
The sound specified as the Windows Question sound.

</td>
</tr>
<tr>
<td>
<dl>
<dt><b>MB_ICONSTOP</b></dt>
<dt>0x00000010L</dt>
</dl>
</td>
<td>
See <b>MB_ICONERROR</b>.

</td>
</tr>
<tr>
<td>
<dl>
<dt><b>MB_ICONWARNING</b></dt>
<dt>0x00000030L</dt>
</dl>
</td>
<td>
The sound specified as the Windows Exclamation sound.

</td>
</tr>
<tr>
<td>
<dl>
<dt><b>MB_OK</b></dt>
<dt>0x00000000L</dt>
</dl>
</td>
<td>
The sound specified as the Windows Default Beep sound.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



After queuing the sound, the <b>MessageBeep</b> function 
    returns control to the calling function and plays the sound asynchronously.

If it cannot play the specified alert sound, 
    <b>MessageBeep</b> attempts to play the system default sound. If 
    it cannot play the system default sound, the function produces a standard beep sound through the computer 
    speaker.

The user can disable the warning beep by using the Sound control panel application.

<b>Note</b>  To send a beep to a remote client, use the <a href="https://msdn.microsoft.com/ea74fe2a-759e-4466-bef4-6061643ddd26">Beep</a> function. 
     The <b>Beep</b> function is redirected to the client, whereas 
     <b>MessageBeep</b> is not.




## -see-also




<a href="https://msdn.microsoft.com/ea74fe2a-759e-4466-bef4-6061643ddd26">Beep</a>



<a href="https://msdn.microsoft.com/ae8ad3a2-1f1a-46d6-adaa-74c50c07dcc5">Error Handling Functions</a>



<a href="https://msdn.microsoft.com/c4af997d-5cb8-4d5d-ae8d-1e0cc724fe02">FlashWindow</a>



<a href="https://msdn.microsoft.com/35b6e93c-323a-4592-9394-a2e9dd79d9e6">Notifying the User</a>
 

 


---
UID: NF:winuser.MessageBeep
title: MessageBeep function (winuser.h)
description: Plays a waveform sound. The waveform sound for each sound type is identified by an entry in the registry.
helpviewer_keywords: ["MessageBeep","MessageBeep function","_win32_messagebeep","base.messagebeep","winuser/MessageBeep"]
old-location: base\messagebeep.htm
tech.root: Debug
ms.assetid: 70681472-36a5-4ae3-b769-0421cf97ff2a
ms.date: 12/05/2018
ms.keywords: MessageBeep, MessageBeep function, _win32_messagebeep, base.messagebeep, winuser/MessageBeep
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MessageBeep
 - winuser/MessageBeep
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-misc-l1-7-0.dll
 - ext-ms-win-ntuser-misc-l1-6-0.dll
 - User32.dll
 - Ext-MS-Win-NTUser-Misc-l1-1-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-2-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-3-0.dll
 - ext-ms-win-ntuser-misc-l1-3-1.dll
 - Ext-MS-Win-NTUser-Misc-L1-4-0.dll
 - Ext-Ms-Win-NTUser-Misc-L1-5-0.dll
 - Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
 - MessageBeep
req.apiset: ext-ms-win-ntuser-misc-l1-1-0 (introduced in Windows 8)
---

# MessageBeep function


## -description

Plays a waveform sound. The waveform sound for each sound type is identified by an entry in the 
    registry.<div> </div><div class="alert"><b>Note</b>  On Windows Server 2022, the Microsoft\Windows\Multimedia\SystemSoundsService task in Task Scheduler is disabled. This task will need to be enabled for MessageBeep to function.</div>

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
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

After queuing the sound, the <b>MessageBeep</b> function 
    returns control to the calling function and plays the sound asynchronously.

If it cannot play the specified alert sound, 
    <b>MessageBeep</b> attempts to play the system default sound. If 
    it cannot play the system default sound, the function produces a standard beep sound using the
    <a href="/windows/desktop/api/utilapiset/nf-utilapiset-beep">Beep</a>
    function. Starting in Windows 7, this plays a simple tone on the default sound device.
    See the documentation for the <b>Beep</b> function for further details.

The user can disable the warning beep by using the Sound control panel application.

<b>Note</b>  To send a beep to a remote client, use the <a href="/windows/desktop/api/utilapiset/nf-utilapiset-beep">Beep</a> function. 
     The <b>Beep</b> function is redirected to the client, whereas 
     <b>MessageBeep</b> is not.

## -see-also

<a href="/windows/desktop/api/utilapiset/nf-utilapiset-beep">Beep</a>



<a href="/windows/desktop/Debug/error-handling-functions">Error Handling Functions</a>



<a href="/windows/desktop/api/winuser/nf-winuser-flashwindow">FlashWindow</a>



<a href="/windows/desktop/Debug/notifying-the-user">Notifying the User</a>

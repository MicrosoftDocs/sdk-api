---
UID: NF:winuser.SoundSentry
title: SoundSentry function (winuser.h)
description: Triggers a visual signal to indicate that a sound is playing.
helpviewer_keywords: ["SoundSentry","SoundSentry function [Windows and Messages]","_win32_SoundSentry","_win32_soundsentry_cpp","winmsg.soundsentry","winui._win32_soundsentry","winuser/SoundSentry"]
old-location: winmsg\soundsentry.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\soundsentry.htm
ms.date: 12/05/2018
ms.keywords: SoundSentry, SoundSentry function [Windows and Messages], _win32_SoundSentry, _win32_soundsentry_cpp, winmsg.soundsentry, winui._win32_soundsentry, winuser/SoundSentry
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - SoundSentry
 - winuser/SoundSentry
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-window-l1-1-6.dll
 - ext-ms-win-ntuser-window-l1-1-5.dll
 - User32.dll
 - Ext-MS-Win-NTUser-Window-l1-1-0.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - SoundSentry
req.apiset: ext-ms-win-ntuser-window-l1-1-0 (introduced in Windows 8)
---

# SoundSentry function


## -description

Triggers a visual signal to indicate that a sound is playing.



## -returns

Type: <b>BOOL</b>

This function returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
The visual signal was or will be displayed correctly.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
An error prevented the signal from being displayed.

</td>
</tr>
</table>

## -remarks

Set the notification behavior by calling <a href="/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa">SystemParametersInfo</a> with the <b>SPI_SETSOUNDSENTRY</b> value.

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/winuser/ns-winuser-soundsentrya">SOUNDSENTRY</a>



<a href="/previous-versions/windows/desktop/legacy/dd373647(v=vs.85)">SoundSentryProc</a>

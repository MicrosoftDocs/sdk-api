---
UID: NF:winuser.SoundSentry
title: SoundSentry function
author: windows-sdk-content
description: Triggers a visual signal to indicate that a sound is playing.
old-location: winmsg\soundsentry.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\soundsentry.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: SoundSentry, SoundSentry function [Windows and Messages], _win32_SoundSentry, _win32_soundsentry_cpp, winmsg.soundsentry, winui._win32_soundsentry, winuser/SoundSentry
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-Window-l1-1-0.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - SoundSentry
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SoundSentry function


## -description


Triggers a visual signal to indicate that a sound is playing. 


## -parameters






## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

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



Set the notification behavior by calling <a href="https://msdn.microsoft.com/9b99465c-e12d-413c-8e69-b46b52f2f11f">SystemParametersInfo</a> with the <b>SPI_SETSOUNDSENTRY</b> value.




## -see-also




<b>Reference</b>



<a href="_win32_SOUNDSENTRY_str">SOUNDSENTRY</a>



<a href="_win32_SoundSentryProc">SoundSentryProc</a>
 

 


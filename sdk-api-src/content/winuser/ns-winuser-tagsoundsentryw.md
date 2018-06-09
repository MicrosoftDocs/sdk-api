---
UID: NS:winuser.tagSOUNDSENTRYW
title: tagSOUNDSENTRYW
author: windows-sdk-content
description: Contains information about the SoundSentry accessibility feature. When the SoundSentry feature is on, the computer displays a visual indication only when a sound is generated.
old-location: winauto\soundsentry.htm
old-project: WinAuto
ms.assetid: a6000966-886b-4b9e-8df2-fee79d494f2e
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: "*LPSOUNDSENTRYW, LPSOUNDSENTRY, LPSOUNDSENTRY structure pointer [Windows Accessibility], SOUNDSENTRY, SOUNDSENTRY structure [Windows Accessibility], SOUNDSENTRYW, SSF_AVAILABLE, SSF_INDICATOR, SSF_SOUNDSENTRYON, SSGF_DISPLAY, SSGF_NONE, SSTF_BORDER, SSTF_CHARS, SSTF_DISPLAY, SSTF_NONE, SSWF_CUSTOM, SSWF_DISPLAY, SSWF_NONE, SSWF_TITLE, SSWF_WINDOW, _win32_SOUNDSENTRY_str, msaa.soundsentry, tagSOUNDSENTRYA, tagSOUNDSENTRYW, winauto.soundsentry, winuser/LPSOUNDSENTRY, winuser/SOUNDSENTRY"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winuser.h
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
tech.root: 
req.typenames: SOUNDSENTRYW, *LPSOUNDSENTRYW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - SOUNDSENTRY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# tagSOUNDSENTRYW structure


## -description



        Contains information about the SoundSentry accessibility feature. When the SoundSentry feature is on, the computer displays a visual indication only when a sound is generated.

<b>Windows 95/98:</b>  The visual indication is displayed
        when a sound is generated through the computer's internal
        speaker.

<b>Windows NT/2000:</b>  The visual indication is displayed
        when a sound is generated through either the multimedia
        sound services or through the computer's speaker.


## -struct-fields




### -field cbSize

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Specifies the size, in bytes, of this structure.


### -field dwFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>


A set of bit flags that specify properties of the SoundSentry feature. The following bit-flag values are defined:



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SSF_AVAILABLE"></a><a id="ssf_available"></a><dl>
<dt><b>SSF_AVAILABLE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the SoundSentry feature is available.

</td>
</tr>
<tr>
<td width="40%"><a id="SSF_INDICATOR"></a><a id="ssf_indicator"></a><dl>
<dt><b>SSF_INDICATOR</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
This flag is not implemented.

</td>
</tr>
<tr>
<td width="40%"><a id="SSF_SOUNDSENTRYON"></a><a id="ssf_soundsentryon"></a><dl>
<dt><b>SSF_SOUNDSENTRYON</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the SoundSentry feature is on.

</td>
</tr>
</table>
 


### -field iFSTextEffect

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>


<b>Windows 95/98:</b> Specifies the visual signal to present when a text-mode application generates a sound while running in a full-screen virtual machine. This member can be one of the following values:



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SSTF_BORDER"></a><a id="sstf_border"></a><dl>
<dt><b>SSTF_BORDER</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Flash the screen border (that is, the overscan area), which is unavailable on some displays.

</td>
</tr>
<tr>
<td width="40%"><a id="SSTF_CHARS"></a><a id="sstf_chars"></a><dl>
<dt><b>SSTF_CHARS</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Flash characters in the corner of the screen.

</td>
</tr>
<tr>
<td width="40%"><a id="SSTF_DISPLAY"></a><a id="sstf_display"></a><dl>
<dt><b>SSTF_DISPLAY</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Flash the entire display.

</td>
</tr>
<tr>
<td width="40%"><a id="SSTF_NONE"></a><a id="sstf_none"></a><dl>
<dt><b>SSTF_NONE</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
No visual signal

</td>
</tr>
</table>
 

<b>Windows NT/2000:</b> This member is reserved for future use. It must be set to zero.


### -field iFSTextEffectMSec

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

<b>Windows 95/98:</b> Specifies the duration, in milliseconds, of the visual signal that is displayed when a full-screen, text-mode application generates a sound.

<b>Windows NT/2000:</b> This member is reserved for future use. It must be set to zero.


### -field iFSTextEffectColorBits

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

<b>Windows 95/98:</b> Specifies the RGB value of the color to be used when displaying the visual signal shown when a full-screen, text-mode application generates a sound.

<b>Windows NT/2000:</b> This member is reserved for future use. It must be set to zero.


### -field iFSGrafEffect

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>


<b>Windows 95/98:</b> Specifies the visual signal to present when a graphics-mode application generates a sound while running in a full-screen virtual machine. This member can be one of the following values:



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SSGF_DISPLAY"></a><a id="ssgf_display"></a><dl>
<dt><b>SSGF_DISPLAY</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Flash the entire display.

</td>
</tr>
<tr>
<td width="40%"><a id="SSGF_NONE"></a><a id="ssgf_none"></a><dl>
<dt><b>SSGF_NONE</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
No visual signal.

</td>
</tr>
</table>
 

<b>Windows NT/2000:</b> This member is reserved for future use. It must be set to zero.


### -field iFSGrafEffectMSec

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

<b>Windows 95/98:</b> Specifies the duration, in milliseconds, of the visual signal that is displayed when a full-screen, graphics-mode application generates a sound.

<b>Windows NT/2000:</b> This member is reserved for future use. It must be set to zero.


### -field iFSGrafEffectColor

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

<b>Windows 95/98:</b> Specifies the RGB value of the color to be used when displaying the visual signal shown when a full-screen, graphics-mode application generates a sound.

<b>Windows NT/2000:</b> This member is reserved for future use. It must be set to zero.


### -field iWindowsEffect

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>


Specifies the visual signal to display when a sound is generated by a Windows-based application or an MS-DOS application running in a window. This member can be one of the following values:



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SSWF_CUSTOM"></a><a id="sswf_custom"></a><dl>
<dt><b>SSWF_CUSTOM</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Use a custom visual signal.

</td>
</tr>
<tr>
<td width="40%"><a id="SSWF_DISPLAY"></a><a id="sswf_display"></a><dl>
<dt><b>SSWF_DISPLAY</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Flash the entire display.

</td>
</tr>
<tr>
<td width="40%"><a id="SSWF_NONE"></a><a id="sswf_none"></a><dl>
<dt><b>SSWF_NONE</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
No visual signal.

</td>
</tr>
<tr>
<td width="40%"><a id="SSWF_TITLE"></a><a id="sswf_title"></a><dl>
<dt><b>SSWF_TITLE</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Flash the title bar of the active window.

</td>
</tr>
<tr>
<td width="40%"><a id="SSWF_WINDOW"></a><a id="sswf_window"></a><dl>
<dt><b>SSWF_WINDOW</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Flash the active window.

</td>
</tr>
</table>
 


### -field iWindowsEffectMSec

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

<b>Windows 95/98:</b> Specifies the duration, in milliseconds, of the visual signal that is displayed when a Win32-based application (or an application running in a window) generates a sound.

<b>Windows NT/2000:</b> This member is reserved for future use. It must be set to zero.


### -field lpszWindowsEffectDLL

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPTSTR</a></b>

This member is reserved for future use. It should be set to <b>NULL</b>.


### -field iWindowsEffectOrdinal

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

This member is reserved for future use. It must be set to zero.


## -remarks



An application uses a <b>SOUNDSENTRY</b> structure when calling the <a href="https://msdn.microsoft.com/9b99465c-e12d-413c-8e69-b46b52f2f11f">SystemParametersInfo</a> function with the <i>uiAction</i> parameter set to <b>SPI_GETSOUNDSENTRY</b> or <b>SPI_SETSOUNDSENTRY</b>. When using <b>SPI_GETSOUNDSENTRY</b>, an application must specify the <b>cbSize</b> member of the <b>SOUNDSENTRY</b> structure; the <b>SystemParametersInfo</b> function fills the remaining members. An application must specify the <b>cbSize</b>, <b>dwFlags</b>, and <b>iWindowsEffect</b> members when using the <b>SPI_SETSOUNDSENTRY</b> value.




## -see-also




<a href="https://msdn.microsoft.com/0ff480ae-18e3-413d-b208-a67fbae28c25">Accessibility Structures</a>



<a href="https://msdn.microsoft.com/49221a97-fbe5-4800-b63e-c49295c8cff2">SoundSentryProc</a>



<a href="https://msdn.microsoft.com/9b99465c-e12d-413c-8e69-b46b52f2f11f">SystemParametersInfo</a>
 

 


---
UID: NS:winuser.tagTITLEBARINFO
title: tagTITLEBARINFO
author: windows-sdk-content
description: Contains title bar information.
old-location: winmsg\titlebarinfo.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowstructures\titlebarinfo.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPTITLEBARINFO, *PTITLEBARINFO, LPTITLEBARINFO, LPTITLEBARINFO structure pointer [Windows and Messages], PTITLEBARINFO, PTITLEBARINFO structure pointer [Windows and Messages], STATE_SYSTEM_FOCUSABLE, STATE_SYSTEM_INVISIBLE, STATE_SYSTEM_OFFSCREEN, STATE_SYSTEM_PRESSED, STATE_SYSTEM_UNAVAILABLE, TITLEBARINFO, TITLEBARINFO structure [Windows and Messages], _win32_TITLEBARINFO_str, _win32_titlebarinfo_str_cpp, tagTITLEBARINFO, winmsg.titlebarinfo, winui._win32_titlebarinfo_str, winuser/LPTITLEBARINFO, winuser/PTITLEBARINFO, winuser/TITLEBARINFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winuser.h
req.include-header: Windows.h
req.redist: 
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
req.typenames: TITLEBARINFO, *PTITLEBARINFO, *LPTITLEBARINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - TITLEBARINFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# tagTITLEBARINFO structure


## -description


Contains title bar information.


## -struct-fields




### -field cbSize

Type: <b>DWORD</b>

The size, in bytes, of the structure. The caller must set this member to <code>sizeof(TITLEBARINFO)</code>. 


### -field rcTitleBar

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a></b>

The coordinates of the title bar. These coordinates include all title-bar elements except the window menu. 


### -field rgstate

Type: <b>DWORD[CCHILDREN_TITLEBAR+1]</b>

An array that receives a 
					value for each element of the title bar. The following are the title bar elements represented by the array. 
					

<table class="clsStd">
<tr>
<th>Index</th>
<th>Title Bar Element</th>
</tr>
<tr>
<td>0</td>
<td>The title bar itself.</td>
</tr>
<tr>
<td>1</td>
<td>Reserved.</td>
</tr>
<tr>
<td>2</td>
<td>Minimize button.</td>
</tr>
<tr>
<td>3</td>
<td>Maximize button.</td>
</tr>
<tr>
<td>4</td>
<td>Help button.</td>
</tr>
<tr>
<td>5</td>
<td>Close button.</td>
</tr>
</table>
 

Each array element is a combination of one or more of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="STATE_SYSTEM_FOCUSABLE"></a><a id="state_system_focusable"></a><dl>
<dt><b>STATE_SYSTEM_FOCUSABLE</b></dt>
<dt>0x00100000</dt>
</dl>
</td>
<td width="60%">
The element can accept the focus.

</td>
</tr>
<tr>
<td width="40%"><a id="STATE_SYSTEM_INVISIBLE"></a><a id="state_system_invisible"></a><dl>
<dt><b>STATE_SYSTEM_INVISIBLE</b></dt>
<dt>0x00008000</dt>
</dl>
</td>
<td width="60%">
The element is invisible.

</td>
</tr>
<tr>
<td width="40%"><a id="STATE_SYSTEM_OFFSCREEN"></a><a id="state_system_offscreen"></a><dl>
<dt><b>STATE_SYSTEM_OFFSCREEN</b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
The element has no visible representation.

</td>
</tr>
<tr>
<td width="40%"><a id="STATE_SYSTEM_UNAVAILABLE"></a><a id="state_system_unavailable"></a><dl>
<dt><b>STATE_SYSTEM_UNAVAILABLE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The element is unavailable.

</td>
</tr>
<tr>
<td width="40%"><a id="STATE_SYSTEM_PRESSED"></a><a id="state_system_pressed"></a><dl>
<dt><b>STATE_SYSTEM_PRESSED</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
The element is in the pressed state.

</td>
</tr>
</table>
 


## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms633513(v=VS.85).aspx">GetTitleBarInfo</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/e2c778c7-7319-4bf7-a6a7-b526e4f3e98b">Windows</a>
 

 


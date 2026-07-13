---
UID: NS:winuser.FLASHWINFO
title: FLASHWINFO (winuser.h)
description: Contains the flash status for a window and the number of times the system should flash the window.
helpviewer_keywords: ["*PFLASHWINFO","FLASHWINFO","FLASHWINFO structure","FLASHW_ALL","FLASHW_CAPTION","FLASHW_STOP","FLASHW_TIMER","FLASHW_TIMERNOFG","FLASHW_TRAY","PFLASHWINFO","PFLASHWINFO structure pointer","_win32_flashwinfo_str","base.flashwinfo_str","winuser/FLASHWINFO","winuser/PFLASHWINFO"]
old-location: base\flashwinfo_str.htm
tech.root: Debug
ms.assetid: b16636bc-fa77-4eb9-9801-dc2cdf0556e5
ms.date: 12/05/2018
ms.keywords: '*PFLASHWINFO, FLASHWINFO, FLASHWINFO structure, FLASHW_ALL, FLASHW_CAPTION, FLASHW_STOP, FLASHW_TIMER, FLASHW_TIMERNOFG, FLASHW_TRAY, PFLASHWINFO, PFLASHWINFO structure pointer, _win32_flashwinfo_str, base.flashwinfo_str, winuser/FLASHWINFO, winuser/PFLASHWINFO'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FLASHWINFO, *PFLASHWINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PFLASHWINFO
 - winuser/PFLASHWINFO
 - FLASHWINFO
 - winuser/FLASHWINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - FLASHWINFO
---

# FLASHWINFO structure


## -description

Contains the flash status for a window and the number of times the system should flash the window.

## -struct-fields

### -field cbSize

The size of the structure, in bytes.

### -field hwnd

A handle to the window to be flashed. The window can be either opened or minimized.

### -field dwFlags

The flash status. This parameter can be one or more of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FLASHW_ALL"></a><a id="flashw_all"></a><dl>
<dt><b>FLASHW_ALL</b></dt>
<dt>0x00000003</dt>
</dl>
</td>
<td width="60%">
Flash both the window caption and taskbar button. This is equivalent to setting the FLASHW_CAPTION | FLASHW_TRAY flags.

</td>
</tr>
<tr>
<td width="40%"><a id="FLASHW_CAPTION"></a><a id="flashw_caption"></a><dl>
<dt><b>FLASHW_CAPTION</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Flash the window caption.

</td>
</tr>
<tr>
<td width="40%"><a id="FLASHW_STOP"></a><a id="flashw_stop"></a><dl>
<dt><b>FLASHW_STOP</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Stop flashing. The system restores the window to its original state.

</td>
</tr>
<tr>
<td width="40%"><a id="FLASHW_TIMER"></a><a id="flashw_timer"></a><dl>
<dt><b>FLASHW_TIMER</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Flash continuously, until the FLASHW_STOP flag is set.

</td>
</tr>
<tr>
<td width="40%"><a id="FLASHW_TIMERNOFG"></a><a id="flashw_timernofg"></a><dl>
<dt><b>FLASHW_TIMERNOFG</b></dt>
<dt>0x0000000C</dt>
</dl>
</td>
<td width="60%">
Flash continuously until the window comes to the foreground.

</td>
</tr>
<tr>
<td width="40%"><a id="FLASHW_TRAY"></a><a id="flashw_tray"></a><dl>
<dt><b>FLASHW_TRAY</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Flash the taskbar button.

</td>
</tr>
</table>

### -field uCount

The number of times to flash the window.

### -field dwTimeout

The rate at which the window is to be flashed, in milliseconds. If <b>dwTimeout</b> is zero, the function uses the default caret blink rate.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-flashwindowex">FlashWindowEx</a>


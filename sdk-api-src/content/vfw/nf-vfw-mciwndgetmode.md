---
UID: NF:vfw.MCIWndGetMode
title: MCIWndGetMode macro (vfw.h)
description: The MCIWndGetMode macro retrieves the current operating mode of an MCI device. MCI devices have several operating modes, which are designated by constants. You can use this macro or explicitly send the MCIWNDM_GETMODE message.
helpviewer_keywords: ["MCIWndGetMode","MCIWndGetMode macro [Windows Multimedia]","_win32_MCIWndGetMode","multimedia.mciwndgetmode","vfw/MCIWndGetMode"]
old-location: multimedia\mciwndgetmode.htm
tech.root: Multimedia
ms.assetid: d5b5d200-459c-4437-9685-1c95e8acc52f
ms.date: 07/01/2025
ms.keywords: MCIWndGetMode, MCIWndGetMode macro [Windows Multimedia], _win32_MCIWndGetMode, multimedia.mciwndgetmode, vfw/MCIWndGetMode
req.header: vfw.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MCIWndGetMode
 - vfw/MCIWndGetMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - MCIWndGetMode
---

# MCIWndGetMode macro

## -syntax

```cpp
LONG MCIWndGetMode(
     hwnd,
     lp,
     len
);
```

## -returns

Type: **LONG**

Returns an integer corresponding to the MCI constant defining the mode.


## -description

The <b>MCIWndGetMode</b> macro retrieves the current operating mode of an MCI device. MCI devices have several operating modes, which are designated by constants. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mciwndm-getmode">MCIWNDM_GETMODE</a> message.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

### -param lp

Pointer to the application-defined buffer used to return the mode.

### -param len

Size, in bytes, of the buffer.

## -remarks

If the null-terminated string describing the mode is longer than the buffer, it is truncated.

Not all devices can operate in every mode. For example, the MCIAVI device is a playback device; it doesn't support the recording mode. The following modes can be retrieved by using <a href="/windows/desktop/Multimedia/mciwndm-getmode">MCIWNDM_GETMODE</a>:

<table>
<tr>
<th>Operating mode
            </th>
<th>MCI constant
            </th>
</tr>
<tr>
<td>not ready</td>
<td>MCI_MODE_NOT_READY</td>
</tr>
<tr>
<td>open</td>
<td>MCI_MODE_OPEN</td>
</tr>
<tr>
<td>paused</td>
<td>MCI_MODE_PAUSE</td>
</tr>
<tr>
<td>playing</td>
<td>MCI_MODE_PLAY</td>
</tr>
<tr>
<td>recording</td>
<td>MCI_MODE_RECORD</td>
</tr>
<tr>
<td>seeking</td>
<td>MCI_MODE_SEEK</td>
</tr>
<tr>
<td>stopped</td>
<td>MCI_MODE_STOP</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/Multimedia/mciwndm-getmode">MCIWNDM_GETMODE</a>

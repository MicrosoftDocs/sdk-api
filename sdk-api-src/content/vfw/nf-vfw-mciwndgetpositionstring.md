---
UID: NF:vfw.MCIWndGetPositionString
title: MCIWndGetPositionString macro (vfw.h)
description: The MCIWndGetPositionString macro retrieves the numerical value of the current position within the content of the MCI device.
helpviewer_keywords: ["MCIWndGetPositionString","MCIWndGetPositionString macro [Windows Multimedia]","_win32_MCIWndGetPositionString","multimedia.mciwndgetpositionstring","vfw/MCIWndGetPositionString"]
old-location: multimedia\mciwndgetpositionstring.htm
tech.root: Multimedia
ms.assetid: ccca1ec7-a523-4a36-bc81-9cb25cfa3aa1
ms.date: 07/01/2025
ms.keywords: MCIWndGetPositionString, MCIWndGetPositionString macro [Windows Multimedia], _win32_MCIWndGetPositionString, multimedia.mciwndgetpositionstring, vfw/MCIWndGetPositionString
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
 - MCIWndGetPositionString
 - vfw/MCIWndGetPositionString
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
 - MCIWndGetPositionString
---

# MCIWndGetPositionString macro

## -syntax

```cpp
LONG MCIWndGetPositionString(
     hwnd,
     lp,
     len
);
```

## -returns

Type: **LONG**

Returns an integer corresponding to the current position. The units for the position value depend on the current time format.


## -description

The <b>MCIWndGetPositionString</b> macro retrieves the numerical value of the current position within the content of the MCI device. This macro also provides the current position in string form in an application-defined buffer. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mciwndm-getposition">MCIWNDM_GETPOSITION</a> message.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

### -param lp

Pointer to an application-defined buffer used to return the position. Use zero to inhibit retrieval of the position as a string. If the device supports tracks, the string position information is returned in the form TT:MM:SS:FF where TT corresponds to tracks, MM and SS correspond to minutes and seconds, and FF corresponds to frames.

### -param len

Size, in bytes, of the buffer. If the null-terminated string is longer than the buffer, it is truncated. Use zero to inhibit retrieval of the position as a string.

## -see-also

<a href="/windows/desktop/Multimedia/mciwndm-getposition">MCIWNDM_GETPOSITION</a>

---
UID: NF:vfw.MCIWndGetFileName
title: MCIWndGetFileName macro (vfw.h)
description: The MCIWndGetFileName macro retrieves the filename used by an MCI device. You can use this macro or explicitly send the MCIWNDM_GETFILENAME message.
helpviewer_keywords: ["MCIWndGetFileName","MCIWndGetFileName macro [Windows Multimedia]","_win32_MCIWndGetFileName","multimedia.mciwndgetfilename","vfw/MCIWndGetFileName"]
old-location: multimedia\mciwndgetfilename.htm
tech.root: Multimedia
ms.assetid: 4118b9fe-4252-4591-862d-a1cc48fa3cff
ms.date: 07/01/2025
ms.keywords: MCIWndGetFileName, MCIWndGetFileName macro [Windows Multimedia], _win32_MCIWndGetFileName, multimedia.mciwndgetfilename, vfw/MCIWndGetFileName
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
 - MCIWndGetFileName
 - vfw/MCIWndGetFileName
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
 - MCIWndGetFileName
---

# MCIWndGetFileName macro

## -syntax

```cpp
LONG MCIWndGetFileName(
     hwnd,
     lp,
     len
);
```

## -returns

Type: **LONG**

Returns zero if successful or 1 otherwise.


## -description

The <b>MCIWndGetFileName</b> macro retrieves the filename used by an MCI device. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mciwndm-getfilename">MCIWNDM_GETFILENAME</a> message.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

### -param lp

Pointer to an application-defined buffer to return the filename.

### -param len

Size, in bytes, of the buffer.

## -remarks

If the null-terminated string containing the filename is longer than the buffer, MCIWnd truncates the filename.

## -see-also

<a href="/windows/desktop/Multimedia/mciwndm-getfilename">MCIWNDM_GETFILENAME</a>

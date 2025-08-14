---
UID: NF:vfw.MCIWndReturnString
title: MCIWndReturnString macro (vfw.h)
description: The MCIWndReturnString macro retrieves the reply to the most recent MCI string command sent to an MCI device. Information in the reply is supplied as a null-terminated string. You can use this macro or explicitly send the MCIWNDM_RETURNSTRING message.
helpviewer_keywords: ["MCIWndReturnString","MCIWndReturnString macro [Windows Multimedia]","_win32_MCIWndReturnString","multimedia.mciwndreturnstring","vfw/MCIWndReturnString"]
old-location: multimedia\mciwndreturnstring.htm
tech.root: Multimedia
ms.assetid: 8e7d54ec-882b-4896-a493-3ed61aec6184
ms.date: 07/01/2025
ms.keywords: MCIWndReturnString, MCIWndReturnString macro [Windows Multimedia], _win32_MCIWndReturnString, multimedia.mciwndreturnstring, vfw/MCIWndReturnString
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
 - MCIWndReturnString
 - vfw/MCIWndReturnString
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
 - MCIWndReturnString
---

# MCIWndReturnString macro

## -syntax

```cpp
LONG MCIWndReturnString(
     hwnd,
     lp,
     len
);
```

## -returns

Type: **LONG**

Returns an integer corresponding to the MCI string.


## -description

The <b>MCIWndReturnString</b> macro retrieves the reply to the most recent MCI string command sent to an MCI device. Information in the reply is supplied as a null-terminated string. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mciwndm-returnstring">MCIWNDM_RETURNSTRING</a> message.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

### -param lp

Pointer to an application-defined buffer to contain the null-terminated string.

### -param len

Size, in bytes, of the buffer.

## -remarks

If the null-terminated string is longer than the buffer, the string is truncated.

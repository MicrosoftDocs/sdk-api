---
UID: NF:vfw.MCIWndClose
title: MCIWndClose macro (vfw.h)
description: The MCIWndClose macro closes an MCI device or file associated with an MCIWnd window.
helpviewer_keywords: ["MCIWndClose","MCIWndClose macro [Windows Multimedia]","_win32_MCIWndClose","multimedia.mciwndclose","vfw/MCIWndClose"]
old-location: multimedia\mciwndclose.htm
tech.root: Multimedia
ms.assetid: f0adc980-c7f6-4937-b844-f65b98047e84
ms.date: 07/01/2025
ms.keywords: MCIWndClose, MCIWndClose macro [Windows Multimedia], _win32_MCIWndClose, multimedia.mciwndclose, vfw/MCIWndClose
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
 - MCIWndClose
 - vfw/MCIWndClose
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
 - MCIWndClose
---

# MCIWndClose macro

## -syntax

```cpp
LONG MCIWndClose(
     hwnd
);
```

## -returns

Type: **LONG**

Returns zero.


## -description

The <b>MCIWndClose</b> macro closes an MCI device or file associated with an MCIWnd window. Although the MCI device closes, the MCIWnd window is still open and can be associated with another MCI device. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mci-close">MCI_CLOSE</a> command.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

## -see-also

<a href="/windows/desktop/Multimedia/mci-close">MCI_CLOSE</a>

---
UID: NF:vfw.MCIWndStop
title: MCIWndStop macro (vfw.h)
description: The MCIWndStop macro stops playing or recording the content of the MCI device associated with the MCIWnd window. You can use this macro or explicitly send the MCI_STOP command.
helpviewer_keywords: ["MCIWndStop","MCIWndStop macro [Windows Multimedia]","_win32_MCIWndStop","multimedia.mciwndstop","vfw/MCIWndStop"]
old-location: multimedia\mciwndstop.htm
tech.root: Multimedia
ms.assetid: e46bca2a-635c-4a80-849d-ee5fc0953161
ms.date: 07/01/2025
ms.keywords: MCIWndStop, MCIWndStop macro [Windows Multimedia], _win32_MCIWndStop, multimedia.mciwndstop, vfw/MCIWndStop
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
 - MCIWndStop
 - vfw/MCIWndStop
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
 - MCIWndStop
---

# MCIWndStop macro

## -syntax

```cpp
LONG MCIWndStop(
     hwnd
);
```

## -returns

Type: **LONG**

Returns zero if successful or an error otherwise.


## -description

The <b>MCIWndStop</b> macro stops playing or recording the content of the MCI device associated with the MCIWnd window. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mci-stop">MCI_STOP</a> command.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

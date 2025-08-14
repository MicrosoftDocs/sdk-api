---
UID: NF:vfw.MCIWndHome
title: MCIWndHome macro (vfw.h)
description: The MCIWndHome macro moves the current position to the beginning of the content. You can use this macro or explicitly send the MCI_SEEK command.
helpviewer_keywords: ["MCIWndHome","MCIWndHome macro [Windows Multimedia]","_win32_MCIWndHome","multimedia.mciwndhome","vfw/MCIWndHome"]
old-location: multimedia\mciwndhome.htm
tech.root: Multimedia
ms.assetid: c028732d-7ead-4417-b3d5-a0df756ad623
ms.date: 07/01/2025
ms.keywords: MCIWndHome, MCIWndHome macro [Windows Multimedia], _win32_MCIWndHome, multimedia.mciwndhome, vfw/MCIWndHome
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
 - MCIWndHome
 - vfw/MCIWndHome
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
 - MCIWndHome
---

# MCIWndHome macro

## -syntax

```cpp
LONG MCIWndHome(
     hwnd
);
```

## -returns

Type: **LONG**

Returns zero if successful or an error otherwise.


## -description

The <b>MCIWndHome</b> macro moves the current position to the beginning of the content. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mci-seek">MCI_SEEK</a> command.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

## -see-also

<a href="/windows/desktop/Multimedia/mci-seek">MCI_SEEK</a>

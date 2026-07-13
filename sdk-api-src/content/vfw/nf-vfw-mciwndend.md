---
UID: NF:vfw.MCIWndEnd
title: MCIWndEnd macro (vfw.h)
description: The MCIWndEnd macro moves the current position to the end of the content. You can use this macro or explicitly send the MCI_SEEK message.
helpviewer_keywords: ["MCIWndEnd","MCIWndEnd macro [Windows Multimedia]","_win32_MCIWndEnd","multimedia.mciwndend","vfw/MCIWndEnd"]
old-location: multimedia\mciwndend.htm
tech.root: Multimedia
ms.assetid: 42704391-cc99-48d1-8274-12621f674708
ms.date: 07/01/2025
ms.keywords: MCIWndEnd, MCIWndEnd macro [Windows Multimedia], _win32_MCIWndEnd, multimedia.mciwndend, vfw/MCIWndEnd
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
 - MCIWndEnd
 - vfw/MCIWndEnd
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
 - MCIWndEnd
---

# MCIWndEnd macro

## -syntax

```cpp
LONG MCIWndEnd(
     hwnd
);
```

## -returns

Type: **LONG**

Returns zero if successful or an error otherwise.


## -description

The <b>MCIWndEnd</b> macro moves the current position to the end of the content. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mci-seek">MCI_SEEK</a> message.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

## -see-also

<a href="/windows/desktop/Multimedia/mci-seek">MCI_SEEK</a>

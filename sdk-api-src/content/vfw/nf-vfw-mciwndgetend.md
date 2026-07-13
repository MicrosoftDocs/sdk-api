---
UID: NF:vfw.MCIWndGetEnd
title: MCIWndGetEnd macro (vfw.h)
description: The MCIWndGetEnd macro retrieves the location of the end of the content of an MCI device or file. You can use this macro or explicitly send the MCIWNDM_GETEND message.
helpviewer_keywords: ["MCIWndGetEnd","MCIWndGetEnd macro [Windows Multimedia]","_win32_MCIWndGetEnd","multimedia.mciwndgetend","vfw/MCIWndGetEnd"]
old-location: multimedia\mciwndgetend.htm
tech.root: Multimedia
ms.assetid: 558d5412-1165-4dda-8ac1-6c599267beaf
ms.date: 07/01/2025
ms.keywords: MCIWndGetEnd, MCIWndGetEnd macro [Windows Multimedia], _win32_MCIWndGetEnd, multimedia.mciwndgetend, vfw/MCIWndGetEnd
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
 - MCIWndGetEnd
 - vfw/MCIWndGetEnd
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
 - MCIWndGetEnd
---

# MCIWndGetEnd macro

## -syntax

```cpp
LONG MCIWndGetEnd(
     hwnd
);
```

## -returns

Type: **LONG**

Returns the location in the current time format.


## -description

The <b>MCIWndGetEnd</b> macro retrieves the location of the end of the content of an MCI device or file. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mciwndm-getend">MCIWNDM_GETEND</a> message.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

## -see-also

<a href="/windows/desktop/Multimedia/mciwndm-getend">MCIWNDM_GETEND</a>

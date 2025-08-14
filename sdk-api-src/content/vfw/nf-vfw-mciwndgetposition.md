---
UID: NF:vfw.MCIWndGetPosition
title: MCIWndGetPosition macro (vfw.h)
description: The MCIWndGetPosition macro retrieves the numerical value of the current position within the content of the MCI device. You can use this macro or explicitly send the MCIWNDM_GETPOSITION message.
helpviewer_keywords: ["MCIWndGetPosition","MCIWndGetPosition macro [Windows Multimedia]","_win32_MCIWndGetPosition","multimedia.mciwndgetposition","vfw/MCIWndGetPosition"]
old-location: multimedia\mciwndgetposition.htm
tech.root: Multimedia
ms.assetid: 317e2d37-432b-41ae-a1ef-66e2dd31a21c
ms.date: 07/01/2025
ms.keywords: MCIWndGetPosition, MCIWndGetPosition macro [Windows Multimedia], _win32_MCIWndGetPosition, multimedia.mciwndgetposition, vfw/MCIWndGetPosition
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
 - MCIWndGetPosition
 - vfw/MCIWndGetPosition
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
 - MCIWndGetPosition
---

# MCIWndGetPosition macro

## -syntax

```cpp
LONG MCIWndGetPosition(
     hwnd
);
```

## -returns

Type: **LONG**

Returns an integer corresponding to the current position. The units for the position value depend on the current time format.


## -description

The <b>MCIWndGetPosition</b> macro retrieves the numerical value of the current position within the content of the MCI device. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mciwndm-getposition">MCIWNDM_GETPOSITION</a> message.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

## -see-also

<a href="/windows/desktop/Multimedia/mciwndm-getposition">MCIWNDM_GETPOSITION</a>

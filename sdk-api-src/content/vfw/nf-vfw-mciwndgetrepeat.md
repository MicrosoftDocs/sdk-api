---
UID: NF:vfw.MCIWndGetRepeat
title: MCIWndGetRepeat macro (vfw.h)
description: The MCIWndGetRepeat macro determines if continuous playback has been activated. You can use this macro or explicitly send the MCIWNDM_GETREPEAT message.
helpviewer_keywords: ["MCIWndGetRepeat","MCIWndGetRepeat macro [Windows Multimedia]","_win32_MCIWndGetRepeat","multimedia.mciwndgetrepeat","vfw/MCIWndGetRepeat"]
old-location: multimedia\mciwndgetrepeat.htm
tech.root: Multimedia
ms.assetid: e5c346db-b33a-4420-b9e1-c634dcffa134
ms.date: 07/01/2025
ms.keywords: MCIWndGetRepeat, MCIWndGetRepeat macro [Windows Multimedia], _win32_MCIWndGetRepeat, multimedia.mciwndgetrepeat, vfw/MCIWndGetRepeat
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
 - MCIWndGetRepeat
 - vfw/MCIWndGetRepeat
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
 - MCIWndGetRepeat
---

# MCIWndGetRepeat macro

## -syntax

```cpp
BOOL MCIWndGetRepeat(
     hwnd
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns **TRUE** if continuous playback is activated or **FALSE** otherwise.


## -description

The <b>MCIWndGetRepeat</b> macro determines if continuous playback has been activated. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mciwndm-getrepeat">MCIWNDM_GETREPEAT</a> message.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

## -see-also

<a href="/windows/desktop/Multimedia/mciwndm-getrepeat">MCIWNDM_GETREPEAT</a>

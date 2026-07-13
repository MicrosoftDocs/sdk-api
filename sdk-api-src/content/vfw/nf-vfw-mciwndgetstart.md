---
UID: NF:vfw.MCIWndGetStart
title: MCIWndGetStart macro (vfw.h)
description: The MCIWndGetStart macro retrieves the location of the beginning of the content of an MCI device or file. You can use this macro or explicitly send the MCIWNDM_GETSTART message.
helpviewer_keywords: ["MCIWndGetStart","MCIWndGetStart macro [Windows Multimedia]","_win32_MCIWndGetStart","multimedia.mciwndgetstart","vfw/MCIWndGetStart"]
old-location: multimedia\mciwndgetstart.htm
tech.root: Multimedia
ms.assetid: fe9346b8-e917-4bbc-9df5-3b0b5c2de306
ms.date: 07/01/2025
ms.keywords: MCIWndGetStart, MCIWndGetStart macro [Windows Multimedia], _win32_MCIWndGetStart, multimedia.mciwndgetstart, vfw/MCIWndGetStart
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
 - MCIWndGetStart
 - vfw/MCIWndGetStart
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
 - MCIWndGetStart
---

# MCIWndGetStart macro

## -syntax

```cpp
LONG MCIWndGetStart(
     hwnd
);
```

## -returns

Type: **LONG**

Returns the location in the current time format. Typically, the return value is zero; but some devices use a nonzero starting location. Seeking to this location sets the device to the start of the media.


## -description

The <b>MCIWndGetStart</b> macro retrieves the location of the beginning of the content of an MCI device or file. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mciwndm-getstart">MCIWNDM_GETSTART</a> message.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

## -see-also

<a href="/windows/desktop/Multimedia/mciwndm-getstart">MCIWNDM_GETSTART</a>

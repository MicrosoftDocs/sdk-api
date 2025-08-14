---
UID: NF:vfw.MCIWndPlayTo
title: MCIWndPlayTo macro (vfw.h)
description: The MCIWndPlayTo macro plays the content of an MCI device from the current position to the specified ending location or until another command stops playback.
helpviewer_keywords: ["MCIWndPlayTo","MCIWndPlayTo macro [Windows Multimedia]","_win32_MCIWndPlayTo","multimedia.mciwndplayto","vfw/MCIWndPlayTo"]
old-location: multimedia\mciwndplayto.htm
tech.root: Multimedia
ms.assetid: 49048776-85bd-43ac-a5a0-414a26a6a533
ms.date: 07/01/2025
ms.keywords: MCIWndPlayTo, MCIWndPlayTo macro [Windows Multimedia], _win32_MCIWndPlayTo, multimedia.mciwndplayto, vfw/MCIWndPlayTo
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
 - MCIWndPlayTo
 - vfw/MCIWndPlayTo
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
 - MCIWndPlayTo
---

# MCIWndPlayTo macro

## -syntax

```cpp
LONG MCIWndPlayTo(
     hwnd,
     lPos
);
```

## -returns

Type: **LONG**

Returns zero if successful or an error otherwise.


## -description

The <b>MCIWndPlayTo</b> macro plays the content of an MCI device from the current position to the specified ending location or until another command stops playback. If the specified ending location is beyond the end of the content, playback stops at the end of the content. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mciwndm-playto">MCIWNDM_PLAYTO</a> message.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

### -param lPos

Ending location. The units for the ending location depend on the current time format.

## -remarks

You can also specify both a starting and ending location for playback by using the <a href="/windows/desktop/api/vfw/nf-vfw-mciwndplayfromto">MCIWndPlayFromTo</a> macro.

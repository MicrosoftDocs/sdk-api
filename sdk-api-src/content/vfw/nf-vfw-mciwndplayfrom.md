---
UID: NF:vfw.MCIWndPlayFrom
title: MCIWndPlayFrom macro (vfw.h)
description: The MCIWndPlayFrom macro plays the content of an MCI device from the specified location to the end of the content or until another command stops playback. You can use this macro or explicitly send the MCIWNDM_PLAYFROM message.
helpviewer_keywords: ["MCIWndPlayFrom","MCIWndPlayFrom macro [Windows Multimedia]","_win32_MCIWndPlayFrom","multimedia.mciwndplayfrom","vfw/MCIWndPlayFrom"]
old-location: multimedia\mciwndplayfrom.htm
tech.root: Multimedia
ms.assetid: b3efd0c9-d216-4b16-818d-76f3bb8f627e
ms.date: 07/01/2025
ms.keywords: MCIWndPlayFrom, MCIWndPlayFrom macro [Windows Multimedia], _win32_MCIWndPlayFrom, multimedia.mciwndplayfrom, vfw/MCIWndPlayFrom
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
 - MCIWndPlayFrom
 - vfw/MCIWndPlayFrom
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
 - MCIWndPlayFrom
---

# MCIWndPlayFrom macro

## -syntax

```cpp
LONG MCIWndPlayFrom(
     hwnd,
     lPos
);
```

## -returns

Type: **LONG**

Returns zero if successful or an error otherwise.


## -description

The <b>MCIWndPlayFrom</b> macro plays the content of an MCI device from the specified location to the end of the content or until another command stops playback. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mciwndm-playfrom">MCIWNDM_PLAYFROM</a> message.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

### -param lPos

Starting location. The units for the starting location depend on the current time format.

## -remarks

You can also specify both a starting and ending location for playback by using the <a href="/windows/desktop/api/vfw/nf-vfw-mciwndplayfromto">MCIWndPlayFromTo</a> macro.

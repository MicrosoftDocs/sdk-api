---
UID: NF:vfw.MCIWndCanPlay
title: MCIWndCanPlay macro (vfw.h)
description: The MCIWndCanPlay macro determines if an MCI device can play a data file or content of some other kind. You can use this macro or explicitly send the MCIWNDM_CAN_PLAY message.
helpviewer_keywords: ["MCIWndCanPlay","MCIWndCanPlay macro [Windows Multimedia]","_win32_MCIWndCanPlay","multimedia.mciwndcanplay","vfw/MCIWndCanPlay"]
old-location: multimedia\mciwndcanplay.htm
tech.root: Multimedia
ms.assetid: 6ba9a080-f74a-4c3d-b264-8fbd768f3e6e
ms.date: 07/01/2025
ms.keywords: MCIWndCanPlay, MCIWndCanPlay macro [Windows Multimedia], _win32_MCIWndCanPlay, multimedia.mciwndcanplay, vfw/MCIWndCanPlay
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
 - MCIWndCanPlay
 - vfw/MCIWndCanPlay
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
 - MCIWndCanPlay
---

# MCIWndCanPlay macro

## -syntax

```cpp
BOOL MCIWndCanPlay(
     hwnd
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns **TRUE** if the device supports playing the data or **FALSE** otherwise.


## -description

The <b>MCIWndCanPlay</b> macro determines if an MCI device can play a data file or content of some other kind. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mciwndm-can-play">MCIWNDM_CAN_PLAY</a> message.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

## -see-also

<a href="/windows/desktop/Multimedia/mciwndm-can-play">MCIWNDM_CAN_PLAY</a>

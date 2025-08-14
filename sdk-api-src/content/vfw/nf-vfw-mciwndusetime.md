---
UID: NF:vfw.MCIWndUseTime
title: MCIWndUseTime macro (vfw.h)
description: The MCIWndUseTime macro sets the time format of an MCI device to milliseconds. You can use this macro or explicitly send the MCIWNDM_SETTIMEFORMAT message.
helpviewer_keywords: ["MCIWndUseTime","MCIWndUseTime macro [Windows Multimedia]","_win32_MCIWndUseTime","multimedia.mciwndusetime","vfw/MCIWndUseTime"]
old-location: multimedia\mciwndusetime.htm
tech.root: Multimedia
ms.assetid: 604031d8-4cb6-49a8-a2c8-7b4966f9cdf4
ms.date: 07/01/2025
ms.keywords: MCIWndUseTime, MCIWndUseTime macro [Windows Multimedia], _win32_MCIWndUseTime, multimedia.mciwndusetime, vfw/MCIWndUseTime
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
 - MCIWndUseTime
 - vfw/MCIWndUseTime
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
 - MCIWndUseTime
---

# MCIWndUseTime macro

## -syntax

```cpp
LONG MCIWndUseTime(
     hwnd
);
```

## -returns

Type: **LONG**

Returns zero if successful or an error otherwise.


## -description

The <b>MCIWndUseTime</b> macro sets the time format of an MCI device to milliseconds. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mciwndm-settimeformat">MCIWNDM_SETTIMEFORMAT</a> message.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

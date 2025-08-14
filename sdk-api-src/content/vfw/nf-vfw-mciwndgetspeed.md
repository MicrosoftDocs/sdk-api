---
UID: NF:vfw.MCIWndGetSpeed
title: MCIWndGetSpeed macro (vfw.h)
description: The MCIWndGetSpeed macro retrieves the playback speed of an MCI device. You can use this macro or explicitly send the MCIWNDM_GETSPEED message.
helpviewer_keywords: ["MCIWndGetSpeed","MCIWndGetSpeed macro [Windows Multimedia]","_win32_MCIWndGetSpeed","multimedia.mciwndgetspeed","vfw/MCIWndGetSpeed"]
old-location: multimedia\mciwndgetspeed.htm
tech.root: Multimedia
ms.assetid: d327b649-8c1e-4219-a1ec-8f89e3a9a33e
ms.date: 07/01/2025
ms.keywords: MCIWndGetSpeed, MCIWndGetSpeed macro [Windows Multimedia], _win32_MCIWndGetSpeed, multimedia.mciwndgetspeed, vfw/MCIWndGetSpeed
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
 - MCIWndGetSpeed
 - vfw/MCIWndGetSpeed
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
 - MCIWndGetSpeed
---

# MCIWndGetSpeed macro

## -syntax

```cpp
LONG MCIWndGetSpeed(
     hwnd
);
```

## -returns

Type: **LONG**

Returns the playback speed if successful. The value for normal speed is 1000. Larger values indicate faster speeds; smaller values indicate slower speeds.


## -description

The <b>MCIWndGetSpeed</b> macro retrieves the playback speed of an MCI device. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mciwndm-getspeed">MCIWNDM_GETSPEED</a> message.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

## -see-also

<a href="/windows/desktop/Multimedia/mciwndm-getspeed">MCIWNDM_GETSPEED</a>

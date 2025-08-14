---
UID: NF:vfw.MCIWndSetVolume
title: MCIWndSetVolume macro (vfw.h)
description: The MCIWndSetVolume macro sets the volume level of an MCI device. You can use this macro or explicitly send the MCIWNDM_SETVOLUME message.
helpviewer_keywords: ["MCIWndSetVolume","MCIWndSetVolume macro [Windows Multimedia]","_win32_MCIWndSetVolume","multimedia.mciwndsetvolume","vfw/MCIWndSetVolume"]
old-location: multimedia\mciwndsetvolume.htm
tech.root: Multimedia
ms.assetid: 4e5da2cd-b83d-4ac3-80e1-d8ac4c6e1c42
ms.date: 07/01/2025
ms.keywords: MCIWndSetVolume, MCIWndSetVolume macro [Windows Multimedia], _win32_MCIWndSetVolume, multimedia.mciwndsetvolume, vfw/MCIWndSetVolume
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
 - MCIWndSetVolume
 - vfw/MCIWndSetVolume
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
 - MCIWndSetVolume
---

# MCIWndSetVolume macro

## -syntax

```cpp
LONG MCIWndSetVolume(
     hwnd,
     iVol
);
```

## -returns

Type: **LONG**

Returns zero if successful or an error otherwise.


## -description

The <b>MCIWndSetVolume</b> macro sets the volume level of an MCI device. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mciwndm-setvolume">MCIWNDM_SETVOLUME</a> message.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

### -param iVol

New volume level. Specify 1000 for normal volume level. Specify a higher value for a louder volume or a lower value for a quieter volume.

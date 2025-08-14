---
UID: NF:vfw.MCIWndGetVolume
title: MCIWndGetVolume macro (vfw.h)
description: The MCIWndGetVolume macro retrieves the current volume setting of an MCI device. You can use this macro or explicitly send the MCIWNDM_GETVOLUME message.
helpviewer_keywords: ["MCIWndGetVolume","MCIWndGetVolume macro [Windows Multimedia]","_win32_MCIWndGetVolume","multimedia.mciwndgetvolume","vfw/MCIWndGetVolume"]
old-location: multimedia\mciwndgetvolume.htm
tech.root: Multimedia
ms.assetid: e5fba475-d7d8-40de-aac7-0188954da180
ms.date: 07/01/2025
ms.keywords: MCIWndGetVolume, MCIWndGetVolume macro [Windows Multimedia], _win32_MCIWndGetVolume, multimedia.mciwndgetvolume, vfw/MCIWndGetVolume
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
 - MCIWndGetVolume
 - vfw/MCIWndGetVolume
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
 - MCIWndGetVolume
---

# MCIWndGetVolume macro

## -syntax

```cpp
LONG MCIWndGetVolume(
     hwnd
);
```

## -returns

Type: **LONG**

Returns the current volume setting. The default value is 1000. Higher values indicate louder volumes; lower values indicate quieter volumes.


## -description

The <b>MCIWndGetVolume</b> macro retrieves the current volume setting of an MCI device. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mciwndm-getvolume">MCIWNDM_GETVOLUME</a> message.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

## -see-also

<a href="/windows/desktop/Multimedia/mciwndm-getvolume">MCIWNDM_GETVOLUME</a>

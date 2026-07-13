---
UID: NF:vfw.MCIWndGetZoom
title: MCIWndGetZoom macro (vfw.h)
description: The MCIWndGetZoom macro retrieves the current zoom value used by an MCI device. You can use this macro or explicitly send the MCIWNDM_GETZOOM message.
helpviewer_keywords: ["MCIWndGetZoom","MCIWndGetZoom macro [Windows Multimedia]","_win32_MCIWndGetZoom","multimedia.mciwndgetzoom","vfw/MCIWndGetZoom"]
old-location: multimedia\mciwndgetzoom.htm
tech.root: Multimedia
ms.assetid: 397a41dd-e4ee-4afb-b7a0-3909e79726a5
ms.date: 07/01/2025
ms.keywords: MCIWndGetZoom, MCIWndGetZoom macro [Windows Multimedia], _win32_MCIWndGetZoom, multimedia.mciwndgetzoom, vfw/MCIWndGetZoom
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
 - MCIWndGetZoom
 - vfw/MCIWndGetZoom
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
 - MCIWndGetZoom
---

# MCIWndGetZoom macro

## -syntax

```cpp
UINT MCIWndGetZoom(
     hwnd
);
```

## -returns

Type: **[UINT](/windows/desktop/winprog/windows-data-types)**

Returns the most recent values used with <a href="/windows/desktop/api/vfw/nf-vfw-mciwndsetzoom">MCIWndSetZoom</a>. A return value of 100 indicates the image is not zoomed. A value of 200 indicates the image is enlarged to twice its original size. A value of 50 indicates the image is reduced to half its original size.


## -description

The <b>MCIWndGetZoom</b> macro retrieves the current zoom value used by an MCI device. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mciwndm-getzoom">MCIWNDM_GETZOOM</a> message.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

## -see-also

<a href="/windows/desktop/Multimedia/mciwndm-getzoom">MCIWNDM_GETZOOM</a>



<a href="/windows/desktop/api/vfw/nf-vfw-mciwndsetzoom">MCIWndSetZoom</a>

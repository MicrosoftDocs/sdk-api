---
UID: NF:vfw.MCIWndRealize
title: MCIWndRealize macro (vfw.h)
description: The MCIWndRealize macro controls how an MCI window realized in the foreground or background. This macro also causes the palette for the MCI window to be realized in the process. You can use this macro or explicitly send the MCIWNDM_REALIZE message.
helpviewer_keywords: ["MCIWndRealize","MCIWndRealize macro [Windows Multimedia]","_win32_MCIWndRealize","multimedia.mciwndrealize","vfw/MCIWndRealize"]
old-location: multimedia\mciwndrealize.htm
tech.root: Multimedia
ms.assetid: 56230397-bdb2-4996-90a1-49c2f9a7e651
ms.date: 07/01/2025
ms.keywords: MCIWndRealize, MCIWndRealize macro [Windows Multimedia], _win32_MCIWndRealize, multimedia.mciwndrealize, vfw/MCIWndRealize
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
 - MCIWndRealize
 - vfw/MCIWndRealize
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
 - MCIWndRealize
---

# MCIWndRealize macro

## -syntax

```cpp
LONG MCIWndRealize(
     hwnd,
     fBkgnd
);
```

## -returns

Type: **LONG**

Returns zero if successful or an error otherwise.


## -description

The <b>MCIWndRealize</b> macro controls how an MCI window realized in the foreground or background. This macro also causes the palette for the MCI window to be realized in the process. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mciwndm-realize">MCIWNDM_REALIZE</a> message.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

### -param fBkgnd

Background flag. Specify <b>TRUE</b> for this parameter for the window to be realized in the background or <b>FALSE</b> if the window can be realized in the foreground.

## -remarks

A common use for <b>MCIWndRealize</b> is to coordinate palette ownership between an MCI control and the application that contains it. The application can have the MCI window realize in the background and realize its own palette in the foreground.

If your application contains an MCI control, but does not need to realize its palette, you can use this macro to handle the WM_PALETTECHANGED and WM_QUERYNEWPALETTE messages, instead of using <b>RealizePalette</b>. However, it is usually easier to call the <b>SendMessage</b> function to forward the message to the MCIWnd window, which will automatically realize the palette.

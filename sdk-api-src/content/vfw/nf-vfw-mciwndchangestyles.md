---
UID: NF:vfw.MCIWndChangeStyles
title: MCIWndChangeStyles macro (vfw.h)
description: The MCIWndChangeStyles macro changes the styles used by the MCIWnd window. You can use this macro or explicitly send the MCIWNDM_CHANGESTYLES message.
helpviewer_keywords: ["MCIWndChangeStyles","MCIWndChangeStyles macro [Windows Multimedia]","_win32_MCIWndChangeStyles","multimedia.mciwndchangestyles","vfw/MCIWndChangeStyles"]
old-location: multimedia\mciwndchangestyles.htm
tech.root: Multimedia
ms.assetid: d87da0b0-4217-421d-a9d5-03602fb2b477
ms.date: 07/01/2025
ms.keywords: MCIWndChangeStyles, MCIWndChangeStyles macro [Windows Multimedia], _win32_MCIWndChangeStyles, multimedia.mciwndchangestyles, vfw/MCIWndChangeStyles
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
 - MCIWndChangeStyles
 - vfw/MCIWndChangeStyles
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
 - MCIWndChangeStyles
---

# MCIWndChangeStyles macro

## -syntax

```cpp
LONG MCIWndChangeStyles(
     hwnd,
     mask,
     value
);
```

## -returns

Type: **LONG**

Returns zero.


## -description

The <b>MCIWndChangeStyles</b> macro changes the styles used by the MCIWnd window. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mciwndm-changestyles">MCIWNDM_CHANGESTYLES</a> message.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

### -param mask

Mask that identifies the styles that can change. This mask is the bitwise OR operator of all styles that will be permitted to change.

### -param value

New style settings for the window. Specify zero for this parameter to turn off all styles identified in the mask. For a list of the available styles, see the MCIWndCreate function.

## -remarks

For an example of using <b>MCIWndChangeStyles</b>, see <a href="/windows/desktop/Multimedia/pausing-and-resuming-playback">Pausing and Resuming Playback</a>.

## -see-also

<a href="/windows/desktop/Multimedia/mciwndm-changestyles">MCIWNDM_CHANGESTYLES</a>

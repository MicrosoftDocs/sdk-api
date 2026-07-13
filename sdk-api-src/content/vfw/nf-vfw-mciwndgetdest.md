---
UID: NF:vfw.MCIWndGetDest
title: MCIWndGetDest macro (vfw.h)
description: The MCIWndGetDest macro retrieves the coordinates of the destination rectangle used for zooming or stretching the images of an AVI file during playback. You can use this macro or explicitly send the MCIWNDM_GET_DEST message.
helpviewer_keywords: ["MCIWndGetDest","MCIWndGetDest macro [Windows Multimedia]","_win32_MCIWndGetDest","multimedia.mciwndgetdest","vfw/MCIWndGetDest"]
old-location: multimedia\mciwndgetdest.htm
tech.root: Multimedia
ms.assetid: eca70819-fb7c-48b9-a479-d20aa0f05649
ms.date: 07/01/2025
ms.keywords: MCIWndGetDest, MCIWndGetDest macro [Windows Multimedia], _win32_MCIWndGetDest, multimedia.mciwndgetdest, vfw/MCIWndGetDest
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
 - MCIWndGetDest
 - vfw/MCIWndGetDest
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
 - MCIWndGetDest
---

# MCIWndGetDest macro

## -syntax

```cpp
UINT MCIWndGetDest(
     hwnd,
     prc
);
```

## -returns

Type: **[UINT](/windows/desktop/winprog/windows-data-types)**

Returns zero if successful or an error otherwise.


## -description

The <b>MCIWndGetDest</b> macro retrieves the coordinates of the destination rectangle used for zooming or stretching the images of an AVI file during playback. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mciwndm-get-dest">MCIWNDM_GET_DEST</a> message.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

### -param prc

Pointer to a RECT structure to return the coordinates of the destination rectangle.

## -see-also

<a href="/windows/desktop/Multimedia/mciwndm-get-dest">MCIWNDM_GET_DEST</a>

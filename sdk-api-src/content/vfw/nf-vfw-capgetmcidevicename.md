---
UID: NF:vfw.capGetMCIDeviceName
title: capGetMCIDeviceName macro (vfw.h)
description: The capGetMCIDeviceName macro retrieves the name of an MCI device previously set with the capSetMCIDeviceName macro. You can use this macro or explicitly call the WM_CAP_GET_MCI_DEVICE message.
helpviewer_keywords: ["_win32_capGetMCIDeviceName","capGetMCIDeviceName","capGetMCIDeviceName macro [Windows Multimedia]","multimedia.capgetmcidevicename","vfw/capGetMCIDeviceName"]
old-location: multimedia\capgetmcidevicename.htm
tech.root: Multimedia
ms.assetid: e65a2a27-ae35-4637-8d85-1cc2162c41b1
ms.date: 07/01/2025
ms.keywords: _win32_capGetMCIDeviceName, capGetMCIDeviceName, capGetMCIDeviceName macro [Windows Multimedia], multimedia.capgetmcidevicename, vfw/capGetMCIDeviceName
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
 - capGetMCIDeviceName
 - vfw/capGetMCIDeviceName
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
 - capGetMCIDeviceName
---

# capGetMCIDeviceName macro

## -syntax

```cpp
BOOL capGetMCIDeviceName(
     hwnd,
     szName,
     wSize
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns **TRUE** if successful or **FALSE** otherwise.


## -description

The <b>capGetMCIDeviceName</b> macro retrieves the name of an MCI device previously set with the <a href="/windows/desktop/api/vfw/nf-vfw-capsetmcidevicename">capSetMCIDeviceName</a> macro. You can use this macro or explicitly call the <a href="/windows/desktop/Multimedia/wm-cap-get-mci-device">WM_CAP_GET_MCI_DEVICE</a> message.

## -parameters

### -param hwnd

Handle to a capture window.

### -param szName

Pointer to a null-terminated string that contains the MCI device name.

### -param wSize

Length, in bytes, of the buffer referenced by <i>szName</i> .

## -see-also

<a href="/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>

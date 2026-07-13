---
UID: NF:vfw.capSetMCIDeviceName
title: capSetMCIDeviceName macro (vfw.h)
description: The capSetMCIDeviceName macro specifies the name of the MCI video device to be used to capture data. You can use this macro or explicitly call the WM_CAP_SET_MCI_DEVICE message.
helpviewer_keywords: ["_win32_capSetMCIDeviceName","capSetMCIDeviceName","capSetMCIDeviceName macro [Windows Multimedia]","multimedia.capsetmcidevicename","vfw/capSetMCIDeviceName"]
old-location: multimedia\capsetmcidevicename.htm
tech.root: Multimedia
ms.assetid: 2dabc360-7f69-4dbb-9826-0657eec265ff
ms.date: 07/01/2025
ms.keywords: _win32_capSetMCIDeviceName, capSetMCIDeviceName, capSetMCIDeviceName macro [Windows Multimedia], multimedia.capsetmcidevicename, vfw/capSetMCIDeviceName
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
 - capSetMCIDeviceName
 - vfw/capSetMCIDeviceName
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
 - capSetMCIDeviceName
---

# capSetMCIDeviceName macro

## -syntax

```cpp
BOOL capSetMCIDeviceName(
     hwnd,
     szName
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns **TRUE** if successful or **FALSE** otherwise.


## -description

The <b>capSetMCIDeviceName</b> macro specifies the name of the MCI video device to be used to capture data. You can use this macro or explicitly call the <a href="/windows/desktop/Multimedia/wm-cap-set-mci-device">WM_CAP_SET_MCI_DEVICE</a> message.

## -parameters

### -param hwnd

Handle to a capture window.

### -param szName

Pointer to a null-terminated string containing the name of the device.

## -remarks

This message stores the MCI device name in an internal structure. It does not open or access the device. The default device name is <b>NULL</b>.

## -see-also

<a href="/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>

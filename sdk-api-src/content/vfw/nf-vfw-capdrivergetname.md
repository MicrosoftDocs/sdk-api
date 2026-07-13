---
UID: NF:vfw.capDriverGetName
title: capDriverGetName macro (vfw.h)
description: The capDriverGetName macro returns the name of the capture driver connected to the capture window. You can use this macro or explicitly call the WM_CAP_DRIVER_GET_NAME message.
helpviewer_keywords: ["_win32_capDriverGetName","capDriverGetName","capDriverGetName macro [Windows Multimedia]","multimedia.capdrivergetname","vfw/capDriverGetName"]
old-location: multimedia\capdrivergetname.htm
tech.root: Multimedia
ms.assetid: 50a5563d-5872-4cfd-a600-be83beceb0fe
ms.date: 07/01/2025
ms.keywords: _win32_capDriverGetName, capDriverGetName, capDriverGetName macro [Windows Multimedia], multimedia.capdrivergetname, vfw/capDriverGetName
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
 - capDriverGetName
 - vfw/capDriverGetName
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
 - capDriverGetName
---

# capDriverGetName macro

## -syntax

```cpp
BOOL capDriverGetName(
     hwnd,
     szName,
     wSize
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns **TRUE** if successful or **FALSE** if the capture window is not connected to a capture driver.


## -description

The <b>capDriverGetName</b> macro returns the name of the capture driver connected to the capture window. You can use this macro or explicitly call the <a href="/windows/desktop/Multimedia/wm-cap-driver-get-name">WM_CAP_DRIVER_GET_NAME</a> message.

## -parameters

### -param hwnd

Handle to a capture window.

### -param szName

Pointer to an application-defined buffer used to return the device name as a null-terminated string.

### -param wSize

Size, in bytes, of the buffer referenced by <i>szName</i>.

## -remarks

The name is a text string retrieved from the driver's resource area. Applications should allocate approximately 80 bytes for this string. If the driver does not contain a name resource, the full path name of the driver listed in the registry or in the SYSTEM.INI file is returned.

## -see-also

<a href="/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>

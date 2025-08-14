---
UID: NF:vfw.capGetUserData
title: capGetUserData macro (vfw.h)
description: The capGetUserData macro retrieves a LONG_PTR data value associated with a capture window. You can use this macro or explicitly call the WM_CAP_GET_USER_DATA message.
helpviewer_keywords: ["_win32_capGetUserData","capGetUserData","capGetUserData macro [Windows Multimedia]","multimedia.capgetuserdata","vfw/capGetUserData"]
old-location: multimedia\capgetuserdata.htm
tech.root: Multimedia
ms.assetid: a71afead-9beb-48d0-9e7f-d948e0fe276f
ms.date: 07/01/2025
ms.keywords: _win32_capGetUserData, capGetUserData, capGetUserData macro [Windows Multimedia], multimedia.capgetuserdata, vfw/capGetUserData
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
 - capGetUserData
 - vfw/capGetUserData
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
 - capGetUserData
---

# capGetUserData macro

## -syntax

```cpp
LPARAM capGetUserData(
     hwnd
);
```

## -returns

Type: **[LPARAM](/windows/desktop/winprog/windows-data-types)**

Returns the value previously saved by using the **capSetUserData** macro.


## -description

The <b>capGetUserData</b> macro retrieves a <b>LONG_PTR</b> data value associated with a capture window. You can use this macro or explicitly call the <a href="/windows/desktop/Multimedia/wm-cap-get-user-data">WM_CAP_GET_USER_DATA</a> message.

## -parameters

### -param hwnd

Handle to a capture window.

## -see-also

<a href="/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>

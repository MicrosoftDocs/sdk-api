---
UID: NF:winuser.GET_POINTERID_WPARAM
title: GET_POINTERID_WPARAM macro (winuser.h)
description: Retrieves the pointer ID using the specified value.
helpviewer_keywords: ["GET_POINTERID_WPARAM","GET_POINTERID_WPARAM","GET_POINTERID_WPARAM macro [Input Messages and Notifications]","inputmsg.get_pointerid_wparam","winuser/GET_POINTERID_WPARAM"]
old-location: inputmsg\get_pointerid_wparam.htm
tech.root: InputMsg
ms.assetid: 31f7dde6-1486-4050-b9b6-ffc2ed991211
ms.date: 07/01/2025
ms.keywords: GET_POINTERID_WPARAM, GET_POINTERID_WPARAM, GET_POINTERID_WPARAM macro [Input Messages and Notifications], inputmsg.get_pointerid_wparam, winuser/GET_POINTERID_WPARAM
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - GET_POINTERID_WPARAM
 - winuser/GET_POINTERID_WPARAM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - GET_POINTERID_WPARAM
---

# GET_POINTERID_WPARAM macro

## -syntax

```cpp
BOOL GET_POINTERID_WPARAM(
    WPARAM wParam
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

The return value is the low-order **int** of the specified value.


## -description

Retrieves the pointer ID using the specified value.

## -parameters

### -param wParam

The value to be converted.

## -see-also

<a href="/windows/win32/inputmsg/macros">Macros</a>

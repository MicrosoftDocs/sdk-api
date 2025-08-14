---
UID: NF:winuser.IS_POINTER_SECONDBUTTON_WPARAM
title: IS_POINTER_SECONDBUTTON_WPARAM macro (winuser.h)
description: Checks whether the specified pointer took second action.
helpviewer_keywords: ["IS_POINTER_SECONDBUTTON_WPARAM","IS_POINTER_SECONDBUTTON_WPARAM","IS_POINTER_SECONDBUTTON_WPARAM macro [Input Messages and Notifications]","inputmsg.is_pointer_secondbutton_wparam","winuser/IS_POINTER_SECONDBUTTON_WPARAM"]
old-location: inputmsg\is_pointer_secondbutton_wparam.htm
tech.root: InputMsg
ms.assetid: 40f7dde6-1486-4050-b9b6-ffc2ed9982a0
ms.date: 07/01/2025
ms.keywords: IS_POINTER_SECONDBUTTON_WPARAM, IS_POINTER_SECONDBUTTON_WPARAM, IS_POINTER_SECONDBUTTON_WPARAM macro [Input Messages and Notifications], inputmsg.is_pointer_secondbutton_wparam, winuser/IS_POINTER_SECONDBUTTON_WPARAM
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
 - IS_POINTER_SECONDBUTTON_WPARAM
 - winuser/IS_POINTER_SECONDBUTTON_WPARAM
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
 - IS_POINTER_SECONDBUTTON_WPARAM
---

# IS_POINTER_SECONDBUTTON_WPARAM macro

## -syntax

```cpp
BOOL IS_POINTER_SECONDBUTTON_WPARAM(
    WPARAM wParam
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

**TRUE** if the specified pointer took second action. Otherwise, **FALSE**.


## -description

Checks whether the specified pointer took second action.

## -parameters

### -param wParam

The value to be converted.

## -see-also

<a href="/windows/win32/inputmsg/macros">Macros</a>

---
UID: NF:winuser.IS_POINTER_FIFTHBUTTON_WPARAM
title: IS_POINTER_FIFTHBUTTON_WPARAM macro (winuser.h)
description: Checks whether the specified pointer took fifth action.
helpviewer_keywords: ["IS_POINTER_FIFTHBUTTON_WPARAM","IS_POINTER_FIFTHBUTTON_WPARAM macro [Input Messages and Notifications]","inputmsg.is_pointer_fifthbutton_wparam","winuser/IS_POINTER_FIFTHBUTTON_WPARAM"]
old-location: inputmsg\is_pointer_fifthbutton_wparam.htm
tech.root: InputMsg
ms.assetid: 181E6E85-9387-4543-B0A1-B1BB66942054
ms.date: 07/01/2025
ms.keywords: IS_POINTER_FIFTHBUTTON_WPARAM, IS_POINTER_FIFTHBUTTON_WPARAM macro [Input Messages and Notifications], inputmsg.is_pointer_fifthbutton_wparam, winuser/IS_POINTER_FIFTHBUTTON_WPARAM
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
 - IS_POINTER_FIFTHBUTTON_WPARAM
 - winuser/IS_POINTER_FIFTHBUTTON_WPARAM
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

# IS_POINTER_FIFTHBUTTON_WPARAM macro

## -syntax

```cpp
BOOL IS_POINTER_SECONDBUTTON_WPARAM(
    WPARAM wParam
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

**TRUE** if the specified pointer took fifth action. Otherwise, **FALSE**.


## -description

Checks whether the specified pointer took fifth action.

## -parameters

### -param wParam

The value to be converted.

## -see-also

<a href="/windows/win32/inputmsg/macros">Macros</a>

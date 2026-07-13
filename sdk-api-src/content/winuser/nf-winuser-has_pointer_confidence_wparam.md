---
UID: NF:winuser.HAS_POINTER_CONFIDENCE_WPARAM
title: HAS_POINTER_CONFIDENCE_WPARAM macro (winuser.h)
description: Checks whether the specified pointer message is considered intentional rather than accidental.
helpviewer_keywords: ["HAS_POINTER_CONFIDENCE_WPARAM","HAS_POINTER_CONFIDENCE_WPARAM macro [Input Messages and Notifications]","inputmsg.has_pointer_confidence_wparam","winuser/HAS_POINTER_CONFIDENCE_WPARAM"]
old-location: inputmsg\has_pointer_confidence_wparam.htm
tech.root: InputMsg
ms.assetid: 58E66EC4-D855-4B24-80E9-54B6DAE6D36C
ms.date: 07/01/2025
ms.keywords: HAS_POINTER_CONFIDENCE_WPARAM, HAS_POINTER_CONFIDENCE_WPARAM macro [Input Messages and Notifications], inputmsg.has_pointer_confidence_wparam, winuser/HAS_POINTER_CONFIDENCE_WPARAM
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
 - HAS_POINTER_CONFIDENCE_WPARAM
 - winuser/HAS_POINTER_CONFIDENCE_WPARAM
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
 - HAS_POINTER_CONFIDENCE_WPARAM
---

# HAS_POINTER_CONFIDENCE_WPARAM macro

## -syntax

```cpp
BOOL HAS_POINTER_CONFIDENCE_WPARAM(
    WPARAM wParam
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

TRUE if the specified pointer is the primary action. Otherwise, FALSE.


## -description

Checks whether the specified pointer message is considered intentional rather than accidental.

## -parameters

### -param wParam

The value to be converted.

## -see-also

<a href="/windows/win32/inputmsg/macros">Macros</a>

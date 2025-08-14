---
UID: NF:winuser.IS_INTRESOURCE
title: IS_INTRESOURCE macro (winuser.h)
description: Determines whether a value is an integer identifier for a resource.
helpviewer_keywords: ["IS_INTRESOURCE","IS_INTRESOURCE macro [Menus and Other Resources]","_win32_IS_INTRESOURCE","_win32_is_intresource_cpp","menurc.is_intresource","winui._win32_is_intresource","winuser/IS_INTRESOURCE"]
old-location: menurc\is_intresource.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcemacros\is_intresource.htm
ms.date: 07/01/2025
ms.keywords: IS_INTRESOURCE, IS_INTRESOURCE macro [Menus and Other Resources], _win32_IS_INTRESOURCE, _win32_is_intresource_cpp, menurc.is_intresource, winui._win32_is_intresource, winuser/IS_INTRESOURCE
req.header: winuser.h
req.include-header: Windows.h
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
 - IS_INTRESOURCE
 - winuser/IS_INTRESOURCE
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
 - IS_INTRESOURCE
---

# IS_INTRESOURCE macro

## -syntax

```cpp
BOOL IS_INTRESOURCE(
    void *_r
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

If the value is a resource identifier, the return value is **TRUE**. Otherwise, the return value is **FALSE**.


## -description

Determines whether a value is an integer identifier for a resource.

## -parameters

### -param _r

The pointer to be tested whether it contains an integer resource identifier.

## -remarks

This macro checks whether all bits except the least 16 bits are zero. When true, <i>_r</i> is an integer identifier for a resource. Otherwise it is typically a pointer to a string.

## -see-also

<a href="/windows/desktop/menurc/resources">Resources Overview</a>

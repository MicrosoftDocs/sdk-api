---
UID: NF:winuser.NEXTRAWINPUTBLOCK
title: NEXTRAWINPUTBLOCK macro (winuser.h)
description: Retrieves the location of the next structure in an array of RAWINPUT structures.
helpviewer_keywords: ["NEXTRAWINPUTBLOCK","NEXTRAWINPUTBLOCK macro [Keyboard and Mouse Input]","_win32_NEXTRAWINPUTBLOCK","_win32_nextrawinputblock_cpp","inputdev.nextrawinputblock","winui._win32_nextrawinputblock","winuser/NEXTRAWINPUTBLOCK"]
old-location: inputdev\nextrawinputblock.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\rawinput\rawinputreference\rawinputmacros\nextrawinputblock.htm
ms.date: 07/01/2025
ms.keywords: NEXTRAWINPUTBLOCK, NEXTRAWINPUTBLOCK macro [Keyboard and Mouse Input], _win32_NEXTRAWINPUTBLOCK, _win32_nextrawinputblock_cpp, inputdev.nextrawinputblock, winui._win32_nextrawinputblock, winuser/NEXTRAWINPUTBLOCK
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - NEXTRAWINPUTBLOCK
 - winuser/NEXTRAWINPUTBLOCK
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
 - NEXTRAWINPUTBLOCK
---

# NEXTRAWINPUTBLOCK macro

## -syntax

```cpp
PRAWINPUT NEXTRAWINPUTBLOCK(
    PRAWINPUT ptr
);
```

## -returns

Type: **PRAWINPUT**

The return value is a pointer to the next structure in the array of <a href="/windows/desktop/api/winuser/ns-winuser-rawinput">RAWINPUT</a> structures.


## -description

Retrieves the location of the next structure in an array of <a href="/windows/desktop/api/winuser/ns-winuser-rawinput">RAWINPUT</a> structures.

## -parameters

### -param ptr

A pointer to a structure in an array of <a href="/windows/desktop/api/winuser/ns-winuser-rawinput">RAWINPUT</a> structures.

## -remarks

This macro is called repeatedly to traverse an array of <a href="/windows/desktop/api/winuser/ns-winuser-rawinput">RAWINPUT</a> structures.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/ns-winuser-rawinput">RAWINPUT</a>



<a href="/windows/desktop/inputdev/raw-input">Raw Input</a>



<b>Reference</b>

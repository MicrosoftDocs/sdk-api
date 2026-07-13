---
UID: NF:commctrl.INDEXTOSTATEIMAGEMASK
title: INDEXTOSTATEIMAGEMASK macro (commctrl.h)
description: Prepares the index of a state image so that a tree-view control or list-view control can use the index to retrieve the state image for an item.
helpviewer_keywords: ["INDEXTOSTATEIMAGEMASK","INDEXTOSTATEIMAGEMASK macro [Windows Controls]","_win32_INDEXTOSTATEIMAGEMASK","_win32_INDEXTOSTATEIMAGEMASK_cpp","commctrl/INDEXTOSTATEIMAGEMASK","controls.INDEXTOSTATEIMAGEMASK","controls._win32_INDEXTOSTATEIMAGEMASK"]
old-location: controls\INDEXTOSTATEIMAGEMASK.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\macros\indextostateimagemask.htm
ms.date: 10/21/2024
ms.keywords: INDEXTOSTATEIMAGEMASK, INDEXTOSTATEIMAGEMASK macro [Windows Controls], _win32_INDEXTOSTATEIMAGEMASK, _win32_INDEXTOSTATEIMAGEMASK_cpp, commctrl/INDEXTOSTATEIMAGEMASK, controls.INDEXTOSTATEIMAGEMASK, controls._win32_INDEXTOSTATEIMAGEMASK
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
 - INDEXTOSTATEIMAGEMASK
 - commctrl/INDEXTOSTATEIMAGEMASK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - INDEXTOSTATEIMAGEMASK
---

# INDEXTOSTATEIMAGEMASK macro

## -syntax

```cpp
UINT INDEXTOSTATEIMAGEMASK(
   UINT i
);
```

## -returns

Type: **[UINT](/windows/desktop/winprog/windows-data-types)**

Returns the index of a state image.


## -description

Prepares the index of a state image so that a tree-view control or list-view control can use the index to retrieve the state image for an item.

## -parameters

### -param i

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The index of a state image.

## -remarks

The <b>INDEXTOSTATEIMAGEMASK</b> macro is defined as follows: 


``` syntax
#define INDEXTOSTATEIMAGEMASK(i) ((i) << 12)
```


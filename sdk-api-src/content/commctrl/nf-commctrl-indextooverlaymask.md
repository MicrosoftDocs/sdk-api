---
UID: NF:commctrl.INDEXTOOVERLAYMASK
title: INDEXTOOVERLAYMASK macro (commctrl.h)
description: Prepares the index of an overlay mask so that the ImageList_Draw function can use it.
helpviewer_keywords: ["INDEXTOOVERLAYMASK","INDEXTOOVERLAYMASK macro [Windows Controls]","_win32_INDEXTOOVERLAYMASK","_win32_INDEXTOOVERLAYMASK_cpp","commctrl/INDEXTOOVERLAYMASK","controls.INDEXTOOVERLAYMASK","controls._win32_INDEXTOOVERLAYMASK"]
old-location: controls\INDEXTOOVERLAYMASK.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\macros\indextooverlaymask.htm
ms.date: 10/21/2024
ms.keywords: INDEXTOOVERLAYMASK, INDEXTOOVERLAYMASK macro [Windows Controls], _win32_INDEXTOOVERLAYMASK, _win32_INDEXTOOVERLAYMASK_cpp, commctrl/INDEXTOOVERLAYMASK, controls.INDEXTOOVERLAYMASK, controls._win32_INDEXTOOVERLAYMASK
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
 - INDEXTOOVERLAYMASK
 - commctrl/INDEXTOOVERLAYMASK
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
 - INDEXTOOVERLAYMASK
---

# INDEXTOOVERLAYMASK macro

## -syntax

```cpp
UINT INDEXTOOVERLAYMASK(
   UINT i
);
```

## -returns

Type: **[UINT](/windows/desktop/winprog/windows-data-types)**

No return value.


## -description

Prepares the index of an overlay mask so that the <a href="/windows/desktop/api/commctrl/nf-commctrl-imagelist_draw">ImageList_Draw</a> function can use it.

## -parameters

### -param i

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

An index of an overlay mask.

## -remarks

The <b>INDEXTOOVERLAYMASK</b> macro is defined as follows.



``` syntax
#define INDEXTOOVERLAYMASK(i) ((i) << 8)
```


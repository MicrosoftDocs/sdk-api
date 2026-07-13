---
UID: NF:dpa_dsa.DPA_SetPtrCount
title: DPA_SetPtrCount macro (dpa_dsa.h)
description: Sets the number of pointers in a dynamic pointer array (DPA).
helpviewer_keywords: ["DPA_SetPtrCount","DPA_SetPtrCount macro [Windows Controls]","_shell_DPA_SetPtrCount","_shell_DPA_SetPtrCount_cpp","controls.DPA_SetPtrCount","controls._shell_DPA_SetPtrCount","dpa_dsa/DPA_SetPtrCount"]
old-location: controls\DPA_SetPtrCount.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\macros\dpa_setptrcount.htm
ms.date: 10/21/2024
ms.keywords: DPA_SetPtrCount, DPA_SetPtrCount macro [Windows Controls], _shell_DPA_SetPtrCount, _shell_DPA_SetPtrCount_cpp, controls.DPA_SetPtrCount, controls._shell_DPA_SetPtrCount, dpa_dsa/DPA_SetPtrCount
req.header: dpa_dsa.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - DPA_SetPtrCount
 - dpa_dsa/DPA_SetPtrCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dpa_dsa.h
api_name:
 - DPA_SetPtrCount
---

# DPA_SetPtrCount macro

## -syntax

```cpp
int DPA_SetPtrCount(
  [in] HDPA hdpa,
  [in] int  cItems
);
```

## -returns

Type: **int**

Returns the number of pointers (elements) the DPA contains.


## -description

Sets the number of pointers in a dynamic pointer array (DPA).

## -parameters

### -param hdpa [in]

A handle to an existing DPA.

### -param cItems [in]

The number of items in the DPA.


---
UID: NF:dpa_dsa.DPA_GetPtrCount
title: DPA_GetPtrCount macro (dpa_dsa.h)
description: Gets the number of pointers in a dynamic pointer array (DPA).
helpviewer_keywords: ["DPA_GetPtrCount","DPA_GetPtrCount macro [Windows Controls]","_shell_DPA_GetPtrCount","_shell_DPA_GetPtrCount_cpp","controls.DPA_GetPtrCount","controls._shell_DPA_GetPtrCount","dpa_dsa/DPA_GetPtrCount"]
old-location: controls\DPA_GetPtrCount.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\macros\dpa_getptrcount.htm
ms.date: 10/21/2024
ms.keywords: DPA_GetPtrCount, DPA_GetPtrCount macro [Windows Controls], _shell_DPA_GetPtrCount, _shell_DPA_GetPtrCount_cpp, controls.DPA_GetPtrCount, controls._shell_DPA_GetPtrCount, dpa_dsa/DPA_GetPtrCount
req.header: dpa_dsa.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - DPA_GetPtrCount
 - dpa_dsa/DPA_GetPtrCount
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
 - DPA_GetPtrCount
---

# DPA_GetPtrCount macro

## -syntax

```cpp
int DPA_GetPtrCount(
  [in] HDPA hdpa
);
```

## -returns

Type: **int**

Returns the number of pointers (elements) the DPA contains.

## -description

Gets the number of pointers in a dynamic pointer array (DPA).

## -parameters

### -param hdpa [in]

A handle to an existing DPA.


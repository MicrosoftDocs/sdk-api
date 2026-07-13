---
UID: NF:dpa_dsa.DPA_FastGetPtr
title: DPA_FastGetPtr macro (dpa_dsa.h)
description: Gets the value of the specified pointer in the dynamic pointer array (DPA).
helpviewer_keywords: ["DPA_FastGetPtr","DPA_FastGetPtr macro [Windows Controls]","_shell_DPA_FastGetPtr","_shell_DPA_FastGetPtr_cpp","controls.DPA_FastGetPtr","controls._shell_DPA_FastGetPtr","dpa_dsa/DPA_FastGetPtr"]
old-location: controls\DPA_FastGetPtr.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\macros\dpa_fastgetptr.htm
ms.date: 10/21/2024
ms.keywords: DPA_FastGetPtr, DPA_FastGetPtr macro [Windows Controls], _shell_DPA_FastGetPtr, _shell_DPA_FastGetPtr_cpp, controls.DPA_FastGetPtr, controls._shell_DPA_FastGetPtr, dpa_dsa/DPA_FastGetPtr
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
 - DPA_FastGetPtr
 - dpa_dsa/DPA_FastGetPtr
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
 - DPA_FastGetPtr
---

# DPA_FastGetPtr macro

## -syntax

```cpp
void DPA_FastGetPtr(
  [in] HDPA hdpa,
  [in] int  i
);
```


## -description

Gets the value of the specified pointer in the dynamic pointer array (DPA).

## -parameters

### -param hdpa [in]

A handle to an existing DPA.

### -param i [in]

The index of the DPA item.

## -remarks

 Unlike function <a href="/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_getptr">DPA_GetPtr</a>, the macro <b>DPA_FastGetPtr</b> does no parameter validation. If the index specified in <b>DPA_FastGetPtr</b> is out of range, the behavior is undefined.

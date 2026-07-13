---
UID: NF:dpa_dsa.DSA_AppendItem
title: DSA_AppendItem macro (dpa_dsa.h)
description: Appends a new item to the end of a dynamic structure array (DSA).
helpviewer_keywords: ["DSA_AppendItem","DSA_AppendItem macro [Windows Controls]","_shell_DSA_AppendItem","_shell_DSA_AppendItem_cpp","controls.DSA_AppendItem","controls._shell_DSA_AppendItem","dpa_dsa/DSA_AppendItem"]
old-location: controls\DSA_AppendItem.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\macros\dsa_appenditem.htm
ms.date: 10/21/2024
ms.keywords: DSA_AppendItem, DSA_AppendItem macro [Windows Controls], _shell_DSA_AppendItem, _shell_DSA_AppendItem_cpp, controls.DSA_AppendItem, controls._shell_DSA_AppendItem, dpa_dsa/DSA_AppendItem
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
 - DSA_AppendItem
 - dpa_dsa/DSA_AppendItem
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
 - DSA_AppendItem
---

# DSA_AppendItem macro

## -syntax

```cpp
int DSA_AppendItem(
  [in] HDSA hdsa,
  [in] void *pitem
);
```

## -returns

Type: **int**

Returns the index of the new item if the append action succeeds, or <code>-1</code> if the append action fails.


## -description

Appends a new item to the end of a dynamic structure array (DSA).

## -parameters

### -param hdsa [in]

A handle to the DSA in which to insert the item.

### -param pitem [in]

A pointer to the item that is to be inserted.

## -remarks

<div class="alert"><b>Note</b>  This macro wraps the <a href="/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_insertitem">DSA_InsertItem</a> function.</div>
<div> </div>
The actual data pointed to by <i>pItem</i> is copied into the DSA. Subsequent actions performed on that item do not affect the original copy.

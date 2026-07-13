---
UID: NF:dpa_dsa.DSA_GetItemCount
title: DSA_GetItemCount macro (dpa_dsa.h)
description: Gets the number of items in a dynamic structure array (DSA).
helpviewer_keywords: ["DSA_GetItemCount","DSA_GetItemCount macro [Windows Controls]","_shell_DSA_GetItemCount","_shell_DSA_GetItemCount_cpp","controls.DSA_GetItemCount","controls._shell_DSA_GetItemCount","dpa_dsa/DSA_GetItemCount"]
old-location: controls\DSA_GetItemCount.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\macros\dsa_getitemcount.htm
ms.date: 10/21/2024
ms.keywords: DSA_GetItemCount, DSA_GetItemCount macro [Windows Controls], _shell_DSA_GetItemCount, _shell_DSA_GetItemCount_cpp, controls.DSA_GetItemCount, controls._shell_DSA_GetItemCount, dpa_dsa/DSA_GetItemCount
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
 - DSA_GetItemCount
 - dpa_dsa/DSA_GetItemCount
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
 - DSA_GetItemCount
---

# DSA_GetItemCount macro

## -syntax

```cpp
int DSA_GetItemCount(
  [in] HDSA hdsa
);
```

## -returns

Type: **int**

Returns the number of items in the DSA.


## -description

Gets the number of items in a dynamic structure array (DSA).

## -parameters

### -param hdsa [in]

A handle to an existing DSA.


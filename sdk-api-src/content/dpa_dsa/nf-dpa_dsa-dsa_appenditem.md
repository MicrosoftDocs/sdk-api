---
UID: NF:dpa_dsa.DSA_AppendItem
title: DSA_AppendItem macro (dpa_dsa.h)
description: Appends a new item to the end of a dynamic structure array (DSA).helpviewer_keywords: ["DSA_AppendItem","DSA_AppendItem macro [Windows Controls]","_shell_DSA_AppendItem","_shell_DSA_AppendItem_cpp","controls.DSA_AppendItem","controls._shell_DSA_AppendItem","dpa_dsa/DSA_AppendItem"]
old-location: controls\DSA_AppendItem.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\macros\dsa_appenditem.htm
ms.date: 12/05/2018
ms.keywords: DSA_AppendItem, DSA_AppendItem macro [Windows Controls], _shell_DSA_AppendItem, _shell_DSA_AppendItem_cpp, controls.DSA_AppendItem, controls._shell_DSA_AppendItem, dpa_dsa/DSA_AppendItem
f1_keywords:
- dpa_dsa/DSA_AppendItem
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- dpa_dsa.h
api_name:
- DSA_AppendItem
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DSA_AppendItem macro


## -description


Appends a new item to the end of a dynamic structure array (DSA).


## -parameters




### -param hdsa [in]

A handle to the DSA in which to insert the item.


### -param pitem [in]

A pointer to the item that is to be inserted.


## -remarks



<div class="alert"><b>Note</b>  This macro wraps the <a href="https://docs.microsoft.com/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_insertitem">DSA_InsertItem</a> function.</div>
<div> </div>
The actual data pointed to by <i>pItem</i> is copied into the DSA. Subsequent actions performed on that item do not affect the original copy.




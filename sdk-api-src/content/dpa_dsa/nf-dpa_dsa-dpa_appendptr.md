---
UID: NF:dpa_dsa.DPA_AppendPtr
title: DPA_AppendPtr macro (dpa_dsa.h)
description: Inserts a new item at the end of a dynamic pointer array (DPA).
helpviewer_keywords: ["DPA_AppendPtr","DPA_AppendPtr macro [Windows Controls]","_shell_DPA_AppendPtr","_shell_DPA_AppendPtr_cpp","controls.DPA_AppendPtr","controls._shell_DPA_AppendPtr","dpa_dsa/DPA_AppendPtr"]
old-location: controls\DPA_AppendPtr.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\macros\dpa_appendptr.htm
ms.date: 12/05/2018
ms.keywords: DPA_AppendPtr, DPA_AppendPtr macro [Windows Controls], _shell_DPA_AppendPtr, _shell_DPA_AppendPtr_cpp, controls.DPA_AppendPtr, controls._shell_DPA_AppendPtr, dpa_dsa/DPA_AppendPtr
f1_keywords:
- dpa_dsa/DPA_AppendPtr
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
- DPA_AppendPtr
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DPA_AppendPtr macro


## -description


Inserts a new item at the end of a dynamic pointer array (DPA).


## -parameters




### -param hdpa

A handle to a DPA.


### -param pitem

A pointer to the item that is to be inserted.


## -remarks



<div class="alert"><b>Note</b>  This macro wraps the <a href="https://docs.microsoft.com/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_insertptr">DPA_InsertPtr</a> function.</div>
<div> </div>



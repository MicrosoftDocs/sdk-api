---
UID: NF:dpa_dsa.DSA_AppendItem
title: DSA_AppendItem macro
author: windows-sdk-content
description: Appends a new item to the end of a dynamic structure array (DSA).
old-location: controls\DSA_AppendItem.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\common\macros\dsa_appenditem.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: DSA_AppendItem, DSA_AppendItem macro [Windows Controls], _shell_DSA_AppendItem, _shell_DSA_AppendItem_cpp, controls.DSA_AppendItem, controls._shell_DSA_AppendItem, dpa_dsa/DSA_AppendItem
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
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
tech.root: 
req.typenames: CRYPTPROTECT_PROMPTSTRUCT, *PCRYPTPROTECT_PROMPTSTRUCT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dpa_dsa.h
api_name:
 - DSA_AppendItem
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# DSA_AppendItem macro


## -description


Appends a new item to the end of a dynamic structure array (DSA).


## -parameters




### -param hdsa

TBD


### -param pitem

TBD






#### - pItem [in]

A pointer to the item that is to be inserted.


#### - pdsa [in]

A handle to the DSA in which to insert the item.


## -remarks



<div class="alert"><b>Note</b>  This macro wraps the <a href="https://msdn.microsoft.com/e7bc2301-ff7b-4ca7-bad8-a323d44ad5ae">DSA_InsertItem</a> function.</div>
<div> </div>
The actual data pointed to by <i>pItem</i> is copied into the DSA. Subsequent actions performed on that item do not affect the original copy.




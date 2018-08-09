---
UID: NF:dpa_dsa.DPA_GetPtrIndex
title: DPA_GetPtrIndex function
author: windows-sdk-content
description: Gets the index of a matching item found in a dynamic pointer array (DPA).
old-location: controls\DPA_GetPtrIndex.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\common\functions\dpa_getptrindex.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DPA_GetPtrIndex, DPA_GetPtrIndex function [Windows Controls], _shell_DPA_GetPtrIndex, _shell_DPA_GetPtrIndex_cpp, controls.DPA_GetPtrIndex, controls._shell_DPA_GetPtrIndex, dpa_dsa/DPA_GetPtrIndex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: dpa_dsa.h
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
tech.root: 
req.typenames: CRYPTPROTECT_PROMPTSTRUCT, *PCRYPTPROTECT_PROMPTSTRUCT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - DPA_GetPtrIndex
product: Windows
targetos: Windows
req.lib: 
req.dll: Comctl32.dll (version 4.0 or later)
req.irql: 
---

# DPA_GetPtrIndex function


## -description


<p class="CCE_Message">[<b>DPA_GetPtrIndex</b> is available through Windows XP with Service Pack 2 (SP2). It might be altered or unavailable in subsequent versions.]

Gets the index of a matching item found in a dynamic pointer array (DPA).


## -parameters




### -param hdpa [in]

Type: <b>HDPA</b>

A handle to an existing DPA.


### -param p [in]

Type: <b>const void*</b>

A pointer to an item to locate in <i>hdpa</i>.


## -returns



Type: <b>int</b>

The index of the item pointed to by <i>pvoid</i>, if found; otherwise, -1.




## -remarks



<b>DPA_GetPtrIndex</b> is not exported by name. To use it, you must use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> and request ordinal 333 from ComCtl32.dll to obtain a function pointer.




---
UID: NF:dpa_dsa.DPA_GetPtrIndex
title: DPA_GetPtrIndex function (dpa_dsa.h)
description: Gets the index of a matching item found in a dynamic pointer array (DPA).
helpviewer_keywords: ["DPA_GetPtrIndex","DPA_GetPtrIndex function [Windows Controls]","_shell_DPA_GetPtrIndex","_shell_DPA_GetPtrIndex_cpp","controls.DPA_GetPtrIndex","controls._shell_DPA_GetPtrIndex","dpa_dsa/DPA_GetPtrIndex"]
old-location: controls\DPA_GetPtrIndex.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\functions\dpa_getptrindex.htm
ms.date: 12/05/2018
ms.keywords: DPA_GetPtrIndex, DPA_GetPtrIndex function [Windows Controls], _shell_DPA_GetPtrIndex, _shell_DPA_GetPtrIndex_cpp, controls.DPA_GetPtrIndex, controls._shell_DPA_GetPtrIndex, dpa_dsa/DPA_GetPtrIndex
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
req.lib: 
req.dll: Comctl32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DPA_GetPtrIndex
 - dpa_dsa/DPA_GetPtrIndex
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - DPA_GetPtrIndex
req.apiset: ext-ms-win-shell-comctl32-da-l1-1-0 (introduced in Windows 10, version 10.0.14393)
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

<b>DPA_GetPtrIndex</b> is not exported by name. To use it, you must use <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> and request ordinal 333 from ComCtl32.dll to obtain a function pointer.

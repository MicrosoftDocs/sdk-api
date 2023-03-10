---
UID: NF:dpa_dsa.DSA_SetItem
title: DSA_SetItem function (dpa_dsa.h)
description: Sets the contents of an element in a dynamic structure array (DSA).
helpviewer_keywords: ["DSA_SetItem","DSA_SetItem function [Windows Controls]","_shell_DSA_SetItem","_shell_DSA_SetItem_cpp","controls.DSA_SetItem","controls._shell_DSA_SetItem","dpa_dsa/DSA_SetItem"]
old-location: controls\DSA_SetItem.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\functions\dsa_setitem.htm
ms.date: 12/05/2018
ms.keywords: DSA_SetItem, DSA_SetItem function [Windows Controls], _shell_DSA_SetItem, _shell_DSA_SetItem_cpp, controls.DSA_SetItem, controls._shell_DSA_SetItem, dpa_dsa/DSA_SetItem
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
 - DSA_SetItem
 - dpa_dsa/DSA_SetItem
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
 - DSA_SetItem
req.apiset: ext-ms-win-shell-comctl32-da-l1-1-0 (introduced in Windows 10, version 10.0.14393)
---

# DSA_SetItem function


## -description

<p class="CCE_Message">[<b>DSA_SetItem</b> is available through Windows XP with Service Pack 2 (SP2). It might be altered or unavailable in subsequent versions.]

Sets the contents of an element in a dynamic structure array (DSA).

## -parameters

### -param hdsa [in]

Type: <b>HDSA</b>

A handle to an existing DSA that contains the element.

### -param i [in]

Type: <b>int</b>

The zero-based index of the item to set.

### -param pitem [in]

Type: <b>void*</b>

A pointer to the item that will replace the specified item in the array.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> if successful; otherwise, <b>FALSE</b>.

## -remarks

<b>DSA_SetItem</b> is not exported by name. To use it, you must use <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> and request ordinal 325 from ComCtl32.dll to obtain a function pointer.

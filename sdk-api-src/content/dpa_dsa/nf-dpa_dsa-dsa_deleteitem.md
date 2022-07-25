---
UID: NF:dpa_dsa.DSA_DeleteItem
title: DSA_DeleteItem function (dpa_dsa.h)
description: Deletes an item from a dynamic structure array (DSA).
helpviewer_keywords: ["DSA_DeleteItem","DSA_DeleteItem function [Windows Controls]","_shell_DSA_DeleteItem","_shell_DSA_DeleteItem_cpp","controls.DSA_DeleteItem","controls._shell_DSA_DeleteItem","dpa_dsa/DSA_DeleteItem"]
old-location: controls\DSA_DeleteItem.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\functions\dsa_deleteitem.htm
ms.date: 12/05/2018
ms.keywords: DSA_DeleteItem, DSA_DeleteItem function [Windows Controls], _shell_DSA_DeleteItem, _shell_DSA_DeleteItem_cpp, controls.DSA_DeleteItem, controls._shell_DSA_DeleteItem, dpa_dsa/DSA_DeleteItem
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
 - DSA_DeleteItem
 - dpa_dsa/DSA_DeleteItem
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
 - DSA_DeleteItem
req.apiset: ext-ms-win-shell-comctl32-da-l1-1-0 (introduced in Windows 10, version 10.0.14393)
---

# DSA_DeleteItem function


## -description

<p class="CCE_Message">[<b>DSA_DeleteItem</b> is available through Windows XP with Service Pack 2 (SP2). It might be altered or unavailable in subsequent versions.]

Deletes an item from a dynamic structure array (DSA).

## -parameters

### -param hdsa [in]

Type: <b>HDSA</b>

A handle to an existing DSA.

### -param i [in]

Type: <b>int</b>

The zero-based index of the item to delete.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> if the item was successfully deleted; otherwise, <b>FALSE</b>.

## -remarks

<b>DSA_DeleteItem</b> is not exported by name. To use it, you must use <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> and request ordinal 326 from ComCtl32.dll to obtain a function pointer.

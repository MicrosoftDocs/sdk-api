---
UID: NF:dpa_dsa.DSA_InsertItem
title: DSA_InsertItem function (dpa_dsa.h)
description: Inserts a new item into a dynamic structure array (DSA). If necessary, the DSA expands to accommodate the new item.
helpviewer_keywords: ["DSA_InsertItem","DSA_InsertItem function [Windows Controls]","_win32_DSA_InsertItem","_win32_DSA_InsertItem_cpp","controls.DSA_InsertItem","controls._win32_DSA_InsertItem","dpa_dsa/DSA_InsertItem"]
old-location: controls\DSA_InsertItem.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\functions\dsa_insertitem.htm
ms.date: 12/05/2018
ms.keywords: DSA_InsertItem, DSA_InsertItem function [Windows Controls], _win32_DSA_InsertItem, _win32_DSA_InsertItem_cpp, controls.DSA_InsertItem, controls._win32_DSA_InsertItem, dpa_dsa/DSA_InsertItem
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
req.lib: Comctl32.lib
req.dll: ComCtl32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DSA_InsertItem
 - dpa_dsa/DSA_InsertItem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ComCtl32.dll
api_name:
 - DSA_InsertItem
req.apiset: ext-ms-win-shell-comctl32-da-l1-1-0 (introduced in Windows 10, version 10.0.14393)
---

# DSA_InsertItem function


## -description

<p class="CCE_Message">[<b>DSA_InsertItem</b> is available for use in the operating 

systems specified in the Requirements section. It may be altered or unavailable in 

subsequent versions.]

Inserts a new item into a dynamic structure array (DSA). If necessary, the DSA expands to accommodate the new item.

## -parameters

### -param hdsa [in]

Type: <b>HDSA</b>

A handle to the DSA in which to insert the item.

### -param i [in]

Type: <b>int</b>

The position in the DSA where new item is to be inserted, or DSA_APPEND to insert the item at the end of the array.

### -param pitem [in]

Type: <b>void*</b>

A pointer to the item that is to be inserted.

## -returns

Type: <b>int</b>

Returns the index of the new item if the insertion succeeds, or DSA_ERR (<code>-1</code>) if the insertion fails.

## -remarks

The actual data pointed to by <i>pItem</i> is copied into the DSA. Subsequent actions performed on that item do not affect the original copy.


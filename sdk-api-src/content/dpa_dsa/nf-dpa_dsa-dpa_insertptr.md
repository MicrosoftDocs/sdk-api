---
UID: NF:dpa_dsa.DPA_InsertPtr
title: DPA_InsertPtr function (dpa_dsa.h)
description: Inserts a new item at a specified position in a dynamic pointer array (DPA). If necessary, the DPA expands to accommodate the new item.
helpviewer_keywords: ["DPA_InsertPtr","DPA_InsertPtr function [Windows Controls]","_win32_DPA_InsertPtr","_win32_DPA_InsertPtr_cpp","controls.DPA_InsertPtr","controls._win32_DPA_InsertPtr","dpa_dsa/DPA_InsertPtr"]
old-location: controls\DPA_InsertPtr.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\functions\dpa_insertptr.htm
ms.date: 12/05/2018
ms.keywords: DPA_InsertPtr, DPA_InsertPtr function [Windows Controls], _win32_DPA_InsertPtr, _win32_DPA_InsertPtr_cpp, controls.DPA_InsertPtr, controls._win32_DPA_InsertPtr, dpa_dsa/DPA_InsertPtr
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
 - DPA_InsertPtr
 - dpa_dsa/DPA_InsertPtr
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
 - DPA_InsertPtr
req.apiset: ext-ms-win-shell-comctl32-da-l1-1-0 (introduced in Windows 10, version 10.0.14393)
---

# DPA_InsertPtr function


## -description

<p class="CCE_Message">[<b>DPA_InsertPtr</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Inserts a new item at a specified position in a dynamic pointer array (DPA). If necessary, the DPA expands to accommodate the new item.

## -parameters

### -param hdpa

Type: <b>HDPA</b>

A handle to a DPA.

### -param i

Type: <b>int</b>

Tbe position where new item is to be inserted.

### -param p

Type: <b>void*</b>

A pointer to the item that is to be inserted.

## -returns

Type: <b>int</b>

Returns the index of the new item or <code>-1</code>, if the insertion fails.


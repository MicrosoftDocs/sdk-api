---
UID: NF:dpa_dsa.DPA_SetPtr
title: DPA_SetPtr function (dpa_dsa.h)
description: Assigns a value to an item in a dynamic pointer array (DPA).
helpviewer_keywords: ["DPA_SetPtr","DPA_SetPtr function [Windows Controls]","_win32_DPA_SetPtr","_win32_DPA_SetPtr_cpp","controls.DPA_SetPtr","controls._win32_DPA_SetPtr","dpa_dsa/DPA_SetPtr"]
old-location: controls\DPA_SetPtr.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\functions\dpa_setptr.htm
ms.date: 12/05/2018
ms.keywords: DPA_SetPtr, DPA_SetPtr function [Windows Controls], _win32_DPA_SetPtr, _win32_DPA_SetPtr_cpp, controls.DPA_SetPtr, controls._win32_DPA_SetPtr, dpa_dsa/DPA_SetPtr
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
 - DPA_SetPtr
 - dpa_dsa/DPA_SetPtr
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
 - DPA_SetPtr
req.apiset: ext-ms-win-shell-comctl32-da-l1-1-0 (introduced in Windows 10, version 10.0.14393)
---

# DPA_SetPtr function


## -description

<p class="CCE_Message">[<b>DPA_SetPtr</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Assigns a value to an item in a dynamic pointer array (DPA).

## -parameters

### -param hdpa

Type: <b>HDPA</b>

A handle to a DPA.

### -param i

Type: <b>int</b>

The index of the item in the DPA. 

<div class="alert"><b>Note</b>  If the index is beyond the current size of the DPA, the DPA expands to accommodate it. You do not need to assign items contiguously.</div>
<div> </div>

### -param p

Type: <b>void*</b>

A pointer to the value to assign to the specified DPA item.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.

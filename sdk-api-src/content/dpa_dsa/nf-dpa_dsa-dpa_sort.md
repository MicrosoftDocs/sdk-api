---
UID: NF:dpa_dsa.DPA_Sort
title: DPA_Sort function (dpa_dsa.h)
description: Sorts the items in a Dynamic Pointer Array (DPA).
helpviewer_keywords: ["DPA_Sort","DPA_Sort function [Windows Controls]","_win32_DPA_Sort","_win32_DPA_Sort_cpp","controls.DPA_Sort","controls._win32_DPA_Sort","dpa_dsa/DPA_Sort"]
old-location: controls\DPA_Sort.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\functions\dpa_sort.htm
ms.date: 12/05/2018
ms.keywords: DPA_Sort, DPA_Sort function [Windows Controls], _win32_DPA_Sort, _win32_DPA_Sort_cpp, controls.DPA_Sort, controls._win32_DPA_Sort, dpa_dsa/DPA_Sort
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
 - DPA_Sort
 - dpa_dsa/DPA_Sort
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
 - DPA_Sort
req.apiset: ext-ms-win-shell-comctl32-da-l1-1-0 (introduced in Windows 10, version 10.0.14393)
---

# DPA_Sort function


## -description

<p class="CCE_Message">[<b>DPA_Sort</b> is available for use in the operating 

systems specified in the Requirements section. It may be altered or unavailable in 

subsequent versions.]

Sorts the items in a Dynamic Pointer Array (DPA).

## -parameters

### -param hdpa

Type: <b>HDPA</b>

A handle to a DPA.

### -param pfnCompare

Type: <b><a href="/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndacompare">PFNDPACOMPARE</a></b>

A comparison function pointer. See <a href="/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndacompare">PFNDPACOMPARE</a> for the comparison function prototype.

### -param lParam

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

An additional parameter to be passed to <i>pfnCmp</i>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Returns <b>TRUE</b> on success or <b>FALSE</b> on failure.

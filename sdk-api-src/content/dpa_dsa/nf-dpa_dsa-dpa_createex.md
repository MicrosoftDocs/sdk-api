---
UID: NF:dpa_dsa.DPA_CreateEx
title: DPA_CreateEx function (dpa_dsa.h)
description: Creates a dynamic pointer array (DPA) using a given specified size and heap location.
helpviewer_keywords: ["DPA_CreateEx","DPA_CreateEx function [Windows Controls]","_shell_DPA_CreateEx","_shell_DPA_CreateEx_cpp","controls.DPA_CreateEx","controls._shell_DPA_CreateEx","dpa_dsa/DPA_CreateEx"]
old-location: controls\DPA_CreateEx.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\functions\dpa_createex.htm
ms.date: 12/05/2018
ms.keywords: DPA_CreateEx, DPA_CreateEx function [Windows Controls], _shell_DPA_CreateEx, _shell_DPA_CreateEx_cpp, controls.DPA_CreateEx, controls._shell_DPA_CreateEx, dpa_dsa/DPA_CreateEx
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
req.dll: ComCtl32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DPA_CreateEx
 - dpa_dsa/DPA_CreateEx
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
 - DPA_CreateEx
req.apiset: ext-ms-win-shell-comctl32-da-l1-1-0 (introduced in Windows 10, version 10.0.14393)
---

# DPA_CreateEx function


## -description

Creates a dynamic pointer array (DPA) using a given specified size and heap location.

## -parameters

### -param cpGrow [in]

Type: <b>int</b>

The number of elements by which the array should be expanded, if the DPA needs to be enlarged.

### -param hheap [in, optional]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HANDLE</a></b>

A handle to the heap where the array is stored.

## -returns

Type: <b>HDPA</b>

Returns a handle to a DPA if successful, or <b>NULL</b> if the call fails.

## -remarks

<b>DPA_CreateEx</b> is not exported by name. To use it, you must use <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> and request ordinal 340 from ComCtl32.dll to obtain a function pointer.

## -see-also

<a href="/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_create">DPA_Create</a>

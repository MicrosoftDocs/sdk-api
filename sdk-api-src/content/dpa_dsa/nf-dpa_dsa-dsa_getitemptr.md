---
UID: NF:dpa_dsa.DSA_GetItemPtr
title: DSA_GetItemPtr function (dpa_dsa.h)
description: Gets a pointer to an element from a dynamic structure array (DSA).
helpviewer_keywords: ["DSA_GetItemPtr","DSA_GetItemPtr function [Windows Controls]","_win32_DSA_GetItemPtr","_win32_DSA_GetItemPtr_cpp","controls.DSA_GetItemPtr","controls._win32_DSA_GetItemPtr","dpa_dsa/DSA_GetItemPtr"]
old-location: controls\DSA_GetItemPtr.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\functions\dsa_getitemptr.htm
ms.date: 12/05/2018
ms.keywords: DSA_GetItemPtr, DSA_GetItemPtr function [Windows Controls], _win32_DSA_GetItemPtr, _win32_DSA_GetItemPtr_cpp, controls.DSA_GetItemPtr, controls._win32_DSA_GetItemPtr, dpa_dsa/DSA_GetItemPtr
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
req.dll: ComCtl32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DSA_GetItemPtr
 - dpa_dsa/DSA_GetItemPtr
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
 - DSA_GetItemPtr
req.apiset: ext-ms-win-shell-comctl32-da-l1-1-0 (introduced in Windows 10, version 10.0.14393)
---

# DSA_GetItemPtr function


## -description

<p class="CCE_Message">[<b>DSA_GetItemPtr</b> is available for use in the operating 

systems specified in the Requirements section. It may be altered or unavailable in 

subsequent versions.]

Gets a pointer to an element from a dynamic structure array (DSA).

## -parameters

### -param hdsa [in]

Type: <b>HDSA</b>

A handle to the DSA containing the element.

### -param i [in]

Type: <b>int</b>

The index of the element to be retrieved (zero-based).

## -returns

Returns a pointer to the specified element or <b>NULL</b> if the call fails.

## -remarks

Using the element pointer that this function returns, you can modify the data in that element directly. However, be aware that a subsequent insert or destroy operation could cause this pointer value to become invalid or to point to a different element.


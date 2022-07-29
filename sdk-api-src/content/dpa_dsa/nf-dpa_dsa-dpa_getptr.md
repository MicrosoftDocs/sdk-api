---
UID: NF:dpa_dsa.DPA_GetPtr
title: DPA_GetPtr function (dpa_dsa.h)
description: Gets an item from a dynamic pointer array (DPA).
helpviewer_keywords: ["DPA_GetPtr","DPA_GetPtr function [Windows Controls]","_win32_DPA_GetPtr","_win32_DPA_GetPtr_cpp","controls.DPA_GetPtr","controls._win32_DPA_GetPtr","dpa_dsa/DPA_GetPtr"]
old-location: controls\DPA_GetPtr.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\functions\dpa_getptr.htm
ms.date: 12/05/2018
ms.keywords: DPA_GetPtr, DPA_GetPtr function [Windows Controls], _win32_DPA_GetPtr, _win32_DPA_GetPtr_cpp, controls.DPA_GetPtr, controls._win32_DPA_GetPtr, dpa_dsa/DPA_GetPtr
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
 - DPA_GetPtr
 - dpa_dsa/DPA_GetPtr
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
 - DPA_GetPtr
req.apiset: ext-ms-win-shell-comctl32-da-l1-1-0 (introduced in Windows 10, version 10.0.14393)
---

# DPA_GetPtr function


## -description

<p class="CCE_Message">[<b>DPA_GetPtr</b> is available for use in the operating 

systems specified in the Requirements section. It may be altered or unavailable in 

subsequent versions.]

Gets an item from a dynamic pointer array (DPA).

## -parameters

### -param hdpa

Type: <b>HDPA</b>

A handle to a DPA.

### -param i

Type: <b>int</b>

The index of item to be retrieved.

## -returns

Returns the specified item or <b>NULL</b>, if the call fails.


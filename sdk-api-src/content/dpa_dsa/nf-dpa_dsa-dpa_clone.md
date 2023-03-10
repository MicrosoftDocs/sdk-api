---
UID: NF:dpa_dsa.DPA_Clone
title: DPA_Clone function (dpa_dsa.h)
description: Duplicates a dynamic pointer array (DPA).
helpviewer_keywords: ["DPA_Clone","DPA_Clone function [Windows Controls]","_shell_DPA_Clone","_shell_DPA_Clone_cpp","controls.DPA_Clone","controls._shell_DPA_Clone","dpa_dsa/DPA_Clone"]
old-location: controls\DPA_Clone.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\functions\dpa_clone.htm
ms.date: 12/05/2018
ms.keywords: DPA_Clone, DPA_Clone function [Windows Controls], _shell_DPA_Clone, _shell_DPA_Clone_cpp, controls.DPA_Clone, controls._shell_DPA_Clone, dpa_dsa/DPA_Clone
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
 - DPA_Clone
 - dpa_dsa/DPA_Clone
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
 - DPA_Clone
req.apiset: ext-ms-win-shell-comctl32-da-l1-1-0 (introduced in Windows 10, version 10.0.14393)
---

# DPA_Clone function


## -description

<p class="CCE_Message">[<b>DPA_Clone</b> is available through Windows XP with Service Pack 2 (SP2). It might be altered or unavailable in subsequent versions.]

Duplicates a dynamic pointer array (DPA).

## -parameters

### -param hdpa [in]

Type: <b>const HDPA</b>

A handle to an existing DPA to copy.

### -param hdpaNew [in, out, optional]

Type: <b>HDPA</b>

When <b>NULL</b>, a new array is copied from <i>hdpaSource</i>. 

                    

This parameter can also contain an array created with <a href="/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_create">DPA_Create</a> or <a href="/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_createex">DPA_CreateEx</a>. The data is overwritten but the original delta size and heap handle retained.

## -returns

Type: <b>HDPA</b>

The handle to the new or altered DPA (<i>hdpaNew</i>) if successful; otherwise, <b>NULL</b>.

## -remarks

<b>DPA_Clone</b> is not exported by name or declared in a public header file. To use it, you must use <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> and request ordinal 331 from ComCtl32.dll to obtain a function pointer.

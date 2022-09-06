---
UID: NF:dpa_dsa.DSA_Destroy
title: DSA_Destroy function (dpa_dsa.h)
description: Frees a dynamic structure array (DSA).
helpviewer_keywords: ["DSA_Destroy","DSA_Destroy function [Windows Controls]","_win32_DSA_Destroy","_win32_DSA_Destroy_cpp","controls.DSA_Destroy","controls._win32_DSA_Destroy","dpa_dsa/DSA_Destroy"]
old-location: controls\DSA_Destroy.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\functions\dsa_destroy.htm
ms.date: 12/05/2018
ms.keywords: DSA_Destroy, DSA_Destroy function [Windows Controls], _win32_DSA_Destroy, _win32_DSA_Destroy_cpp, controls.DSA_Destroy, controls._win32_DSA_Destroy, dpa_dsa/DSA_Destroy
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
 - DSA_Destroy
 - dpa_dsa/DSA_Destroy
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
 - DSA_Destroy
req.apiset: ext-ms-win-shell-comctl32-da-l1-1-0 (introduced in Windows 10, version 10.0.14393)
---

# DSA_Destroy function


## -description

<p class="CCE_Message">[<b>DSA_Destroy</b> is available for use in the operating 

systems specified in the Requirements section. It may be altered or unavailable in 

subsequent versions.]

Frees a dynamic structure array (DSA).

## -parameters

### -param hdsa [in]

Type: <b>HDSA</b>

A handle to a DSA to destroy.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Returns <b>TRUE</b> on success, <b>FALSE</b> on failure.

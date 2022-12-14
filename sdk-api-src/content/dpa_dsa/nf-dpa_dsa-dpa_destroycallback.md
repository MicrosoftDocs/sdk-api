---
UID: NF:dpa_dsa.DPA_DestroyCallback
title: DPA_DestroyCallback function (dpa_dsa.h)
description: Calls pfnCB on each element of the dynamic pointer array (DPA), then frees the DPA.
helpviewer_keywords: ["DPA_DestroyCallback","DPA_DestroyCallback function [Windows Controls]","_win32_DPA_DestroyCallback","_win32_DPA_DestroyCallback_cpp","controls.DPA_DestroyCallback","controls._win32_DPA_DestroyCallback","dpa_dsa/DPA_DestroyCallback"]
old-location: controls\DPA_DestroyCallback.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\functions\dpa_destroycallback.htm
ms.date: 12/05/2018
ms.keywords: DPA_DestroyCallback, DPA_DestroyCallback function [Windows Controls], _win32_DPA_DestroyCallback, _win32_DPA_DestroyCallback_cpp, controls.DPA_DestroyCallback, controls._win32_DPA_DestroyCallback, dpa_dsa/DPA_DestroyCallback
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
 - DPA_DestroyCallback
 - dpa_dsa/DPA_DestroyCallback
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
 - DPA_DestroyCallback
req.apiset: ext-ms-win-shell-comctl32-da-l1-1-0 (introduced in Windows 10, version 10.0.14393)
---

# DPA_DestroyCallback function


## -description

<p class="CCE_Message">[<b>DPA_DestroyCallback</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Calls <i>pfnCB</i> on each element of the dynamic pointer array (DPA), then frees the DPA.

## -parameters

### -param hdpa

Type: <b>HDPA</b>

A handle to a DPA.

### -param pfnCB

Type: <b><a href="/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndaenumcallback">PFNDPAENUMCALLBACK</a></b>

A callback function pointer. See <a href="/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndaenumcallback">PFNDPAENUMCALLBACK</a> for the callback function prototype.

### -param pData

Type: <b>void*</b>

A callback data pointer. <i>pData</i> is passed as a parameter to <i>pfnCB</i>.

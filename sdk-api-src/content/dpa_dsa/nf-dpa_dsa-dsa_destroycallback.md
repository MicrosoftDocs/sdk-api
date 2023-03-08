---
UID: NF:dpa_dsa.DSA_DestroyCallback
title: DSA_DestroyCallback function (dpa_dsa.h)
description: Iterates through a dynamic structure array (DSA), calling a specified callback function on each item. Upon reaching the end of the array, the DSA is freed.
helpviewer_keywords: ["DSA_DestroyCallback","DSA_DestroyCallback function [Windows Controls]","_win32_DSA_DestroyCallback","_win32_DSA_DestroyCallback_cpp","controls.DSA_DestroyCallback","controls._win32_DSA_DestroyCallback","dpa_dsa/DSA_DestroyCallback"]
old-location: controls\DSA_DestroyCallback.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\functions\dsa_destroycallback.htm
ms.date: 12/05/2018
ms.keywords: DSA_DestroyCallback, DSA_DestroyCallback function [Windows Controls], _win32_DSA_DestroyCallback, _win32_DSA_DestroyCallback_cpp, controls.DSA_DestroyCallback, controls._win32_DSA_DestroyCallback, dpa_dsa/DSA_DestroyCallback
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
 - DSA_DestroyCallback
 - dpa_dsa/DSA_DestroyCallback
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
 - DSA_DestroyCallback
req.apiset: ext-ms-win-shell-comctl32-da-l1-1-0 (introduced in Windows 10, version 10.0.14393)
---

# DSA_DestroyCallback function


## -description

<p class="CCE_Message">[<b>DSA_DestroyCallback</b> is available for use in the operating 

systems specified in the Requirements section. It may be altered or unavailable in 

subsequent versions.]

Iterates through a dynamic structure array (DSA), calling a specified callback function on each item. Upon reaching the end of the array, the DSA is freed.

## -parameters

### -param hdsa [in]

Type: <b>HDSA</b>

A handle to a DSA to walk and destroy.

### -param pfnCB [in]

Type: <b><a href="/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndaenumcallback">PFNDSAENUMCALLBACK</a></b>

A callback function pointer. For the callback function prototype, see <a href="/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndaenumcallback">PFNDSAENUMCALLBACK</a>.

### -param pData [in]

Type: <b>void*</b>

A callback data pointer. This pointer is, in turn, passed as a parameter to <i>pfnCB</i>.

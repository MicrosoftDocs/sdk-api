---
UID: NF:shlobj_core.SHFree
title: SHFree function (shlobj_core.h)
description: Frees the memory allocated by SHAlloc.
helpviewer_keywords: ["SHFree","SHFree function [Windows Shell]","_win32_SHFree","shell.SHFree","shlobj_core/SHFree"]
old-location: shell\SHFree.htm
tech.root: shell
ms.assetid: c9a532ad-ae24-4505-9e7b-577b90365441
ms.date: 12/05/2018
ms.keywords: SHFree, SHFree function [Windows Shell], _win32_SHFree, shell.SHFree, shlobj_core/SHFree
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHFree
 - shlobj_core/SHFree
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
 - Windows.Storage.dll
api_name:
 - SHFree
---

# SHFree function


## -description

<p class="CCE_Message">[This function is available through Windows XP Service Pack 2 (SP2) and Windows Server 2003. It might be altered or unavailable in subsequent versions of Windows. Use <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> instead.]

Frees the memory allocated by <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shalloc">SHAlloc</a>.

## -parameters

### -param pv [in]

Type: <b>void*</b>

A pointer to the memory allocated by <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shalloc">SHAlloc</a>.
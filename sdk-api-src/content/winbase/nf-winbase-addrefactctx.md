---
UID: NF:winbase.AddRefActCtx
title: AddRefActCtx function (winbase.h)
description: The AddRefActCtx function increments the reference count of the specified activation context.
helpviewer_keywords: ["AddRefActCtx","AddRefActCtx function [Side-by-side Assemblies]","_win32_addrefactctx","setup.addrefactctx","winbase/AddRefActCtx"]
old-location: setup\addrefactctx.htm
tech.root: setup
ms.assetid: 6812a3f4-53e4-4b60-be04-711ab4c37d12
ms.date: 12/05/2018
ms.keywords: AddRefActCtx, AddRefActCtx function [Side-by-side Assemblies], _win32_addrefactctx, setup.addrefactctx, winbase/AddRefActCtx
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AddRefActCtx
 - winbase/AddRefActCtx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-sidebyside-l1-1-0.dll
 - KernelBase.dll
api_name:
 - AddRefActCtx
---

# AddRefActCtx function


## -description

The 
<b>AddRefActCtx</b> function increments the reference count of the specified activation context.

## -parameters

### -param hActCtx [in]

Handle to an 
<a href="/windows/desktop/api/winbase/ns-winbase-actctxa">ACTCTX</a> structure that contains information on the activation context for which the reference count is to be incremented.

## -remarks

This function is provided so that multiple clients can access a single activation context.

## -see-also

<a href="/windows/desktop/api/winbase/ns-winbase-actctxa">ACTCTX</a>
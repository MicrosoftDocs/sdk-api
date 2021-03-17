---
UID: NF:winbase.ZombifyActCtx
title: ZombifyActCtx function (winbase.h)
description: The ZombifyActCtx function deactivates the specified activation context, but does not deallocate it.
helpviewer_keywords: ["ZombifyActCtx","ZombifyActCtx function [Side-by-side Assemblies]","_win32_zombifyactctx","setup.zombifyactctx","winbase/ZombifyActCtx"]
old-location: setup\zombifyactctx.htm
tech.root: setup
ms.assetid: f421350a-66b5-4c5a-9e4c-ef69dbe39e7c
ms.date: 12/05/2018
ms.keywords: ZombifyActCtx, ZombifyActCtx function [Side-by-side Assemblies], _win32_zombifyactctx, setup.zombifyactctx, winbase/ZombifyActCtx
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
 - ZombifyActCtx
 - winbase/ZombifyActCtx
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
 - ZombifyActCtx
---

# ZombifyActCtx function


## -description

The 
<b>ZombifyActCtx</b> function deactivates the specified activation context, but does not deallocate it.

## -parameters

### -param hActCtx [in]

Handle to the activation context that is to be deactivated.

## -returns

If the function succeeds, it returns <b>TRUE</b>. If a <b>null</b> handle is passed in the <i>hActCtx</i> parameter, NULL_INVALID_PARAMETER will be returned. Otherwise, it returns <b>FALSE</b>.

This function sets errors that can be retrieved by calling 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. For an example, see 
<a href="/windows/desktop/Debug/retrieving-the-last-error-code">Retrieving the Last-Error Code</a>. For a complete list of error codes, see 
<a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

This function is intended for use in debugging threads using activation contexts. If the activation context deactivated by this function is subsequently accessed, the access  fails and an assertion failure is shown in the debugger.

## -see-also

<a href="/windows/desktop/api/winbase/ns-winbase-actctxa">ACTCTX</a>
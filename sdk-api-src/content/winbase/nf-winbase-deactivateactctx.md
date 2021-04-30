---
UID: NF:winbase.DeactivateActCtx
title: DeactivateActCtx function (winbase.h)
description: The DeactivateActCtx function deactivates the activation context corresponding to the specified cookie.
helpviewer_keywords: ["0","DEACTIVATE_ACTCTX_FLAG_FORCE_EARLY_DEACTIVATION","DeactivateActCtx","DeactivateActCtx function [Side-by-side Assemblies]","_win32_deactivateactctx","setup.deactivateactctx","winbase/DeactivateActCtx"]
old-location: setup\deactivateactctx.htm
tech.root: setup
ms.assetid: 2a53eb1a-ce0b-4b20-a346-1ff9636a74d6
ms.date: 12/05/2018
ms.keywords: 0, DEACTIVATE_ACTCTX_FLAG_FORCE_EARLY_DEACTIVATION, DeactivateActCtx, DeactivateActCtx function [Side-by-side Assemblies], _win32_deactivateactctx, setup.deactivateactctx, winbase/DeactivateActCtx
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
 - DeactivateActCtx
 - winbase/DeactivateActCtx
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
 - DeactivateActCtx
---

# DeactivateActCtx function


## -description

The 
<b>DeactivateActCtx</b> function deactivates the activation context corresponding to the specified cookie.

## -parameters

### -param dwFlags [in]

Flags that indicate how the deactivation is to occur. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
If this value is set and the cookie specified in the <i>ulCookie</i> parameter is in the top frame of the activation stack, the activation context is popped from the stack and thereby deactivated. 




If this value is set and the cookie specified in the <i>ulCookie</i> parameter is not in the top frame of the activation stack, this function  searches down the stack for the cookie.

If the cookie is found, a STATUS_SXS_EARLY_DEACTIVATION exception is thrown.

If the cookie is not found, a STATUS_SXS_INVALID_DEACTIVATION exception is thrown.

This value should be specified in most cases.

</td>
</tr>
<tr>
<td width="40%"><a id="DEACTIVATE_ACTCTX_FLAG_FORCE_EARLY_DEACTIVATION"></a><a id="deactivate_actctx_flag_force_early_deactivation"></a><dl>
<dt><b>DEACTIVATE_ACTCTX_FLAG_FORCE_EARLY_DEACTIVATION</b></dt>
</dl>
</td>
<td width="60%">
If this value is set and the cookie specified in the <i>ulCookie</i> parameter is in the top frame of the activation stack, the function  returns an ERROR_INVALID_PARAMETER error code. Call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> to obtain this code. 




If this value is set and the cookie is not on the activation stack, a STATUS_SXS_INVALID_DEACTIVATION exception will be thrown.

If this value is set and the cookie is in a lower frame of the activation stack, all of the frames down to and including the frame the cookie is in is popped from the stack.

</td>
</tr>
</table>

### -param ulCookie [in]

The ULONG_PTR that was passed into the call to 
<a href="/windows/desktop/api/winbase/nf-winbase-activateactctx">ActivateActCtx</a>. This value is used as a cookie to identify a specific activated activation context.

## -returns

If the function succeeds, it returns <b>TRUE</b>. Otherwise, it returns <b>FALSE</b>.

This function sets errors that can be retrieved by calling 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. For an example, see 
<a href="/windows/desktop/Debug/retrieving-the-last-error-code">Retrieving the Last-Error Code</a>. For a complete list of error codes, see 
<a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

The deactivation of activation contexts must occur in the reverse order of activation. It can be understood as popping an activation context from a stack.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-activateactctx">ActivateActCtx</a>
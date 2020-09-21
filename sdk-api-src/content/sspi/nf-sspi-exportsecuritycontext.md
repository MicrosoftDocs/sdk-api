---
UID: NF:sspi.ExportSecurityContext
title: ExportSecurityContext function (sspi.h)
description: The ExportSecurityContext function creates a serialized representation of a security context that can later be imported into a different process by calling ImportSecurityContext.
helpviewer_keywords: ["ExportSecurityContext","ExportSecurityContext function [Security]","SECPKG_CONTEXT_EXPORT_DELETE_OLD","SECPKG_CONTEXT_EXPORT_RESET_NEW","SECPKG_CONTEXT_EXPORT_TO_KERNEL","_ssp_exportsecuritycontext","security.exportsecuritycontext","sspi/ExportSecurityContext"]
old-location: security\exportsecuritycontext.htm
tech.root: security
ms.assetid: 4ebc7f37-b948-4c78-973f-0a74e55c7ee2
ms.date: 12/05/2018
ms.keywords: ExportSecurityContext, ExportSecurityContext function [Security], SECPKG_CONTEXT_EXPORT_DELETE_OLD, SECPKG_CONTEXT_EXPORT_RESET_NEW, SECPKG_CONTEXT_EXPORT_TO_KERNEL, _ssp_exportsecuritycontext, security.exportsecuritycontext, sspi/ExportSecurityContext
req.header: sspi.h
req.include-header: Security.h
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
req.lib: Secur32.lib
req.dll: Secur32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ExportSecurityContext
 - sspi/ExportSecurityContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Secur32.dll
api_name:
 - ExportSecurityContext
---

# ExportSecurityContext function


## -description

The <b>ExportSecurityContext</b> function creates a serialized representation of a <a href="/windows/desktop/SecGloss/s-gly">security context</a> that can later be imported into a different process by calling  
<a href="/windows/desktop/api/sspi/nf-sspi-importsecuritycontexta">ImportSecurityContext</a>. The process that imports the security context must be running on the same computer as the process that called <b>ExportSecurityContext</b>.

## -parameters

### -param phContext [in]

A handle of the security context to be exported.

### -param fFlags [in]

This parameter can be a bitwise-<b>OR</b> combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SECPKG_CONTEXT_EXPORT_RESET_NEW"></a><a id="secpkg_context_export_reset_new"></a><dl>
<dt><b>SECPKG_CONTEXT_EXPORT_RESET_NEW</b></dt>
<dt>1 (0x1)</dt>
</dl>
</td>
<td width="60%">
The new security context is reset to its initial state.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_CONTEXT_EXPORT_DELETE_OLD"></a><a id="secpkg_context_export_delete_old"></a><dl>
<dt><b>SECPKG_CONTEXT_EXPORT_DELETE_OLD</b></dt>
<dt>2 (0x2)</dt>
</dl>
</td>
<td width="60%">
The old security context is deleted.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_CONTEXT_EXPORT_TO_KERNEL"></a><a id="secpkg_context_export_to_kernel"></a><dl>
<dt><b>SECPKG_CONTEXT_EXPORT_TO_KERNEL</b></dt>
<dt>4 (0x4)</dt>
</dl>
</td>
<td width="60%">
This value is not supported. 

<b>Windows Server 2003 and Windows XP/2000:  </b>The security context is to be exported to the kernel.This value is supported only in Schannel kernel mode.



</td>
</tr>
</table>

### -param pPackedContext [out]

A pointer to a buffer of type <b>SECBUFFER_EMPTY</b> that receives the <a href="/windows/desktop/SecGloss/s-gly">serialized</a> security context. When you have finished using this context,  free it by calling the 
<a href="/windows/desktop/api/sspi/nf-sspi-freecontextbuffer">FreeContextBuffer</a> function.

### -param pToken [out, optional]

A pointer to receive the handle of the context's token.

When you have finished using the user token, release the handle by calling the <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function.

## -returns

If the function succeeds, the function returns SEC_E_OK.

If the function fails, it returns one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INSUFFICIENT_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory available to complete the requested action.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>phContext</i> parameter does not point to a valid handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
Schannel kernel mode does not support this function.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/sspi/nf-sspi-freecontextbuffer">FreeContextBuffer</a>



<a href="/windows/desktop/api/sspi/nf-sspi-importsecuritycontexta">ImportSecurityContext</a>



<a href="/windows/desktop/SecAuthN/authentication-functions">SSPI Functions</a>
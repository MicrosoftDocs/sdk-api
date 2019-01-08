---
UID: NF:sspi.ExportSecurityContext
title: ExportSecurityContext function
author: windows-sdk-content
description: The ExportSecurityContext function creates a serialized representation of a security context that can later be imported into a different process by calling ImportSecurityContext.
old-location: security\exportsecuritycontext.htm
tech.root: SecAuthN
ms.assetid: 4ebc7f37-b948-4c78-973f-0a74e55c7ee2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ExportSecurityContext, ExportSecurityContext function [Security], SECPKG_CONTEXT_EXPORT_DELETE_OLD, SECPKG_CONTEXT_EXPORT_RESET_NEW, SECPKG_CONTEXT_EXPORT_TO_KERNEL, _ssp_exportsecuritycontext, security.exportsecuritycontext, sspi/ExportSecurityContext
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Secur32.dll
api_name:
 - ExportSecurityContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ExportSecurityContext function


## -description


The <b>ExportSecurityContext</b> function creates a serialized representation of a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a> that can later be imported into a different process by calling  
<a href="https://msdn.microsoft.com/0f8e65d0-69cf-42ba-a903-1922d731e5ec">ImportSecurityContext</a>. The process that imports the security context must be running on the same computer as the process that called <b>ExportSecurityContext</b>.


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

A pointer to a buffer of type <b>SECBUFFER_EMPTY</b> that receives the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">serialized</a> security context. When you have finished using this context,  free it by calling the 
<a href="https://msdn.microsoft.com/3c3d27bb-4f9a-4979-b679-1e10fa1ff221">FreeContextBuffer</a> function.


### -param pToken [out, optional]

A pointer to receive the handle of the context's token.

When you have finished using the user token, release the handle by calling the <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function.


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




<a href="https://msdn.microsoft.com/3c3d27bb-4f9a-4979-b679-1e10fa1ff221">FreeContextBuffer</a>



<a href="https://msdn.microsoft.com/0f8e65d0-69cf-42ba-a903-1922d731e5ec">ImportSecurityContext</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa374731(v=VS.85).aspx">SSPI Functions</a>
 

 


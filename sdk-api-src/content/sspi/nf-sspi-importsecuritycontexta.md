---
UID: NF:sspi.ImportSecurityContextA
title: ImportSecurityContextA function
author: windows-sdk-content
description: Imports a security context. The security context must have been exported to the process calling ImportSecurityContext by a previous call to ExportSecurityContext.
old-location: security\importsecuritycontext.htm
tech.root: secauthn
ms.assetid: 0f8e65d0-69cf-42ba-a903-1922d731e5ec
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: ImportSecurityContext, ImportSecurityContext function [Security], ImportSecurityContextA, ImportSecurityContextW, _ssp_importsecuritycontext, security.importsecuritycontext, sspi/ImportSecurityContext, sspi/ImportSecurityContextA, sspi/ImportSecurityContextW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: sspi.h
req.include-header: Security.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ImportSecurityContextW (Unicode) and ImportSecurityContextA (ANSI)
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
 - sspicli.dll
api_name:
 - ImportSecurityContext
 - ImportSecurityContextA
 - ImportSecurityContextW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ImportSecurityContextA function


## -description


The <b>ImportSecurityContext</b> function imports a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a>. The security context must have been exported to the process calling <b>ImportSecurityContext</b> by a previous call to <a href="https://msdn.microsoft.com/4ebc7f37-b948-4c78-973f-0a74e55c7ee2">ExportSecurityContext</a>.


## -parameters




### -param pszPackage [in]

A string that contains the name of the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a> to which the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a> was exported.


### -param pPackedContext [in]

A pointer to a buffer that contains the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">serialized</a> security context created by <a href="https://msdn.microsoft.com/4ebc7f37-b948-4c78-973f-0a74e55c7ee2">ExportSecurityContext</a>.


### -param Token [in, optional]

A handle to the context's token.


### -param phContext [out]

A handle of the new security context created from <i>pPackedContext</i>. When you have finished using the context, delete it by calling the  <a href="https://msdn.microsoft.com/2a4dd697-ef90-4c37-ab74-0e5ab92794cd">DeleteSecurityContext</a> function.


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
<dt><b>SEC_E_UNKNOWN_CREDENTIALS</b></dt>
</dl>
</td>
<td width="60%">
The credentials supplied to the package were not recognized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_NO_CREDENTIALS</b></dt>
</dl>
</td>
<td width="60%">
No credentials are available in the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_NOT_OWNER</b></dt>
</dl>
</td>
<td width="60%">
The caller of the function does not have the necessary credentials.

</td>
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
<dt><b>SEC_E_INTERNAL_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An error occurred that did not map to an SSPI error code.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/4ebc7f37-b948-4c78-973f-0a74e55c7ee2">ExportSecurityContext</a>



<a href="https://msdn.microsoft.com/3c3d27bb-4f9a-4979-b679-1e10fa1ff221">FreeContextBuffer</a>



<a href="authentication_functions.htm">SSPI Functions</a>
 

 


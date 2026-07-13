---
UID: NF:sspi.ImportSecurityContextW
title: ImportSecurityContextW function (sspi.h)
description: Imports a security context. The security context must have been exported to the process calling ImportSecurityContext by a previous call to ExportSecurityContext. (Unicode)
helpviewer_keywords: ["ImportSecurityContext", "ImportSecurityContext function [Security]", "ImportSecurityContextW", "_ssp_importsecuritycontext", "security.importsecuritycontext", "sspi/ImportSecurityContext", "sspi/ImportSecurityContextW"]
old-location: security\importsecuritycontext.htm
tech.root: security
ms.assetid: 0f8e65d0-69cf-42ba-a903-1922d731e5ec
ms.date: 12/05/2018
ms.keywords: ImportSecurityContext, ImportSecurityContext function [Security], ImportSecurityContextA, ImportSecurityContextW, _ssp_importsecuritycontext, security.importsecuritycontext, sspi/ImportSecurityContext, sspi/ImportSecurityContextA, sspi/ImportSecurityContextW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ImportSecurityContextW
 - sspi/ImportSecurityContextW
dev_langs:
 - c++
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
---

# ImportSecurityContextW function


## -description

The <b>ImportSecurityContext</b> function imports a <a href="/windows/desktop/SecGloss/s-gly">security context</a>. The security context must have been exported to the process calling <b>ImportSecurityContext</b> by a previous call to <a href="/windows/desktop/api/sspi/nf-sspi-exportsecuritycontext">ExportSecurityContext</a>.

## -parameters

### -param pszPackage [in]

A string that contains the name of the <a href="/windows/desktop/SecGloss/s-gly">security package</a> to which the <a href="/windows/desktop/SecGloss/s-gly">security context</a> was exported.

### -param pPackedContext [in]

A pointer to a buffer that contains the <a href="/windows/desktop/SecGloss/s-gly">serialized</a> security context created by <a href="/windows/desktop/api/sspi/nf-sspi-exportsecuritycontext">ExportSecurityContext</a>.

### -param Token [in, optional]

A handle to the context's token.

### -param phContext [out]

A handle of the new security context created from <i>pPackedContext</i>. When you have finished using the context, delete it by calling the  <a href="/windows/desktop/api/sspi/nf-sspi-deletesecuritycontext">DeleteSecurityContext</a> function.

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
No credentials are available in the <a href="/windows/desktop/SecGloss/s-gly">security package</a>.

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

<a href="/windows/desktop/api/sspi/nf-sspi-exportsecuritycontext">ExportSecurityContext</a>



<a href="/windows/desktop/api/sspi/nf-sspi-freecontextbuffer">FreeContextBuffer</a>



<a href="/windows/desktop/SecAuthN/authentication-functions">SSPI Functions</a>

## -remarks

> [!NOTE]
> The sspi.h header defines ImportSecurityContext as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

---
UID: NC:ntsecpkg.SpInitUserModeContextFn
title: SpInitUserModeContextFn (ntsecpkg.h)
description: Creates a user-mode security context from a packed Local Security Authority (LSA)-mode context.
helpviewer_keywords: ["SpInitUserModeContext","SpInitUserModeContext callback function [Security]","SpInitUserModeContextFn","SpInitUserModeContextFn callback","_ssp_spinitusermodecontext","ntsecpkg/SpInitUserModeContext","security.spinitusermodecontext"]
old-location: security\spinitusermodecontext.htm
tech.root: security
ms.assetid: e67a7ad3-b3d2-4c1a-a514-f51ccfaf990e
ms.date: 12/05/2018
ms.keywords: SpInitUserModeContext, SpInitUserModeContext callback function [Security], SpInitUserModeContextFn, SpInitUserModeContextFn callback, _ssp_spinitusermodecontext, ntsecpkg/SpInitUserModeContext, security.spinitusermodecontext
req.header: ntsecpkg.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SpInitUserModeContextFn
 - ntsecpkg/SpInitUserModeContextFn
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ntsecpkg.h
api_name:
 - SpInitUserModeContext
---

# SpInitUserModeContextFn callback function


## -description

The <b>SpInitUserModeContext</b> function creates a user-mode <a href="/windows/desktop/SecGloss/s-gly">security context</a> from a packed <a href="/windows/desktop/SecGloss/l-gly">Local Security Authority</a> (LSA)-mode context.

## -parameters

### -param ContextHandle [in]

A handle to the LSA-mode context returned from the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitlsamodecontextfn">SpInitLsaModeContext</a> or 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spacceptlsamodecontextfn">SpAcceptLsaModeContext</a> function.

### -param PackedContext [in]

Pointer to a 
<a href="/windows/desktop/api/sspi/ns-sspi-secbuffer">SecBuffer</a> structure that contains the <a href="/windows/desktop/SecGloss/s-gly">serialized</a> context data. Use the 
<a href="/windows/desktop/api/sspi/nf-sspi-freecontextbuffer">FreeContextBuffer</a> function to free memory allocated for this structure.

## -returns

If the function succeeds, return STATUS_SUCCESS.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed. The following  lists a common reason for failure and the error code that the function should return.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INSUFFICIENT_RESOURCES</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to create the context.

</td>
</tr>
</table>

## -remarks

The <b>SpInitUserModeContext</b> function is called after a security context has been created by the security package, if the <i>MappedContext</i> parameter of the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitlsamodecontextfn">SpInitLsaModeContext</a> or 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spacceptlsamodecontextfn">SpAcceptLsaModeContext</a> is set to <b>TRUE</b>. The package-specific context data should contain the information required to determine which function resulted in the call to <b>SpInitUserModeContext</b>.

SSP/APs must implement the <b>SpInitUserModeContext</b> function; however, the actual name given to the implementation is up to the developer.

A pointer to the <b>SpInitUserModeContext</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_user_function_table">SECPKG_USER_FUNCTION_TABLE</a> structure received from the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spusermodeinitializefn">SpUserModeInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_user_function_table">SECPKG_USER_FUNCTION_TABLE</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spacceptlsamodecontextfn">SpAcceptLsaModeContext</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitlsamodecontextfn">SpInitLsaModeContext</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spusermodeinitializefn">SpUserModeInitialize</a>
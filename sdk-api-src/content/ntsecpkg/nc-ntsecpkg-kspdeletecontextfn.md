---
UID: NC:ntsecpkg.KspDeleteContextFn
title: KspDeleteContextFn (ntsecpkg.h)
description: Deletes a security context.
helpviewer_keywords: ["KspDeleteContextFn","KspDeleteContextFn callback","SpDeleteContext","SpDeleteContext callback function [Security]","_ssp_spdeletecontext","ntsecpkg/SpDeleteContext","security.spdeletecontext"]
old-location: security\spdeletecontext.htm
tech.root: security
ms.assetid: 70e64bd3-7fdf-464b-bc0a-a0384a3e1a59
ms.date: 12/05/2018
ms.keywords: KspDeleteContextFn, KspDeleteContextFn callback, SpDeleteContext, SpDeleteContext callback function [Security], _ssp_spdeletecontext, ntsecpkg/SpDeleteContext, security.spdeletecontext
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
 - KspDeleteContextFn
 - ntsecpkg/KspDeleteContextFn
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
 - SpDeleteContext
---

# KspDeleteContextFn callback function


## -description

Deletes a <a href="/windows/desktop/SecGloss/s-gly">security context</a>.

## -parameters

### -param ContextId [in]

A handle to the security context to delete.

### -param LsaContextId

## -returns

If the function succeeds, return STATUS_SUCCESS.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed. The following table lists a common reason for failure and the error code that the function should return.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle is not valid.

</td>
</tr>
</table>

## -remarks

SSP/APs must implement the <b>SpDeleteContext</b> function; however, the actual name given to the implementation is up to the developer.

A pointer to the <b>SpDeleteContext</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_function_table">SECPKG_FUNCTION_TABLE</a> structure received from the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-splsamodeinitializefn">SpLsaModeInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_function_table">SECPKG_FUNCTION_TABLE</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-splsamodeinitializefn">SpLsaModeInitialize</a>
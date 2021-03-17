---
UID: NC:ntsecpkg.SpExportSecurityContextFn
title: SpExportSecurityContextFn (ntsecpkg.h)
description: Exports a security context to another process.
helpviewer_keywords: ["SECPKG_CONTEXT_EXPORT_DELETE_OLD","SECPKG_CONTEXT_EXPORT_RESET_NEW","SpExportSecurityContext","SpExportSecurityContext callback function [Security]","SpExportSecurityContextFn","SpExportSecurityContextFn callback","_ssp_spexportsecuritycontext","ntsecpkg/SpExportSecurityContext","security.spexportsecuritycontext"]
old-location: security\spexportsecuritycontext.htm
tech.root: security
ms.assetid: 0c8cafb3-aaf5-4937-91dc-e534bb6e4caf
ms.date: 12/05/2018
ms.keywords: SECPKG_CONTEXT_EXPORT_DELETE_OLD, SECPKG_CONTEXT_EXPORT_RESET_NEW, SpExportSecurityContext, SpExportSecurityContext callback function [Security], SpExportSecurityContextFn, SpExportSecurityContextFn callback, _ssp_spexportsecuritycontext, ntsecpkg/SpExportSecurityContext, security.spexportsecuritycontext
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
 - SpExportSecurityContextFn
 - ntsecpkg/SpExportSecurityContextFn
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
 - SpExportSecurityContext
---

# SpExportSecurityContextFn callback function


## -description

Exports a security context to another process.

The <b>SpExportSecurityContext</b> function is the dispatch function for the 
<a href="/windows/desktop/api/sspi/nf-sspi-exportsecuritycontext">ExportSecurityContext</a> function of the 
<a href="/windows/desktop/SecAuthN/sspi">Security Support Provider Interface</a>.

## -parameters

### -param phContext [in]

A handle to the security context to export.

### -param fFlags [in]

Optional. Specifies context duplication options. The following table lists the valid values which are defined in Sspi.h. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SECPKG_CONTEXT_EXPORT_RESET_NEW"></a><a id="secpkg_context_export_reset_new"></a><dl>
<dt><b>SECPKG_CONTEXT_EXPORT_RESET_NEW</b></dt>
</dl>
</td>
<td width="60%">
New context is reset to initial state.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_CONTEXT_EXPORT_DELETE_OLD"></a><a id="secpkg_context_export_delete_old"></a><dl>
<dt><b>SECPKG_CONTEXT_EXPORT_DELETE_OLD</b></dt>
</dl>
</td>
<td width="60%">
Old context is deleted during export.

</td>
</tr>
</table>

### -param pPackedContext [out]

Pointer to a 
<a href="/windows/desktop/api/sspi/ns-sspi-secbuffer">SecBuffer</a> structure containing the <a href="/windows/desktop/SecGloss/s-gly">serialized</a> context. Resources should be allocated using the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_allocate_client_buffer">AllocateClientBuffer</a> function, and freed by the caller using the 
<a href="/windows/desktop/api/sspi/nf-sspi-freecontextbuffer">FreeContextBuffer</a> function.

### -param pToken [out]

Optional. Pointer to a handle that receives the context's token.

## -returns

If the function succeeds, return STATUS_SUCCESS.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed.

## -remarks

To import a previously exported security context use the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spimportsecuritycontextfn">SpImportSecurityContext</a> function.

SSP/APs must implement the <b>SpExportSecurityContext</b> function; however, the actual name given to the implementation is up to the developer.

A pointer to the <b>SpExportSecurityContext</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_user_function_table">SECPKG_USER_FUNCTION_TABLE</a> structure received from the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spusermodeinitializefn">SpUserModeInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_user_function_table">SECPKG_USER_FUNCTION_TABLE</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spimportsecuritycontextfn">SpImportSecurityContext</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spusermodeinitializefn">SpUserModeInitialize</a>
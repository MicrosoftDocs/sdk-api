---
UID: NC:ntsecpkg.SpQueryContextAttributesFn
title: SpQueryContextAttributesFn (ntsecpkg.h)
author: windows-sdk-content
description: Retrieves the attributes of a security context.
old-location: security\spquerycontextattributes.htm
tech.root: SecAuthN
ms.assetid: 720b37dd-a957-4da9-8b94-4642e515bc22
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SpQueryContextAttributes, SpQueryContextAttributes callback function [Security], SpQueryContextAttributesFn, SpQueryContextAttributesFn callback, _ssp_spquerycontextattributes, ntsecpkg/SpQueryContextAttributes, security.spquerycontextattributes
ms.topic: callback
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ntsecpkg.h
api_name:
 - SpQueryContextAttributes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SpQueryContextAttributesFn callback function


## -description


The <b>SpQueryContextAttributes</b> function retrieves the attributes of a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">security context</a>.

The <b>SpQueryContextAttributes</b> function is the dispatch function for the 
<a href="https://docs.microsoft.com/windows/desktop/api/sspi/nf-sspi-querycontextattributesa">QueryContextAttributes (General)</a> function of the 
<a href="https://docs.microsoft.com/windows/desktop/SecAuthN/sspi">Security Support Provider Interface</a>.


## -parameters




### -param ContextHandle [in]

A handle to the security context.


### -param ContextAttribute [in]

Context attribute to query. For a list of valid values, see the 
<a href="https://docs.microsoft.com/windows/desktop/api/sspi/nf-sspi-querycontextattributesa">QueryContextAttributes (General)</a> function.


### -param Buffer [out]

Pointer that receives the address of a buffer containing the requested attributes. Memory for the <i>Buffer</i> parameter should be allocated with the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)">AllocateHeap</a> function from the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/ns-ntsecpkg-_secpkg_dll_functions">SECPKG_DLL_FUNCTIONS</a> function table in user-mode. In <a href="https://docs.microsoft.com/windows/desktop/SecGloss/l-gly">Local Security Authority</a> (LSA) mode, use the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_allocate_lsa_heap">AllocateLsaHeap</a> function.


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
<dt><b>SEC_E_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle is not valid.

</td>
</tr>
</table>
 




## -remarks



SSP/APs must implement the <b>SpQueryContextAttributes</b> function; however, the actual name given to the implementation is up to the developer.

A pointer to the LSA-mode implementation of the <b>SpQueryContextAttributes</b> function is available in the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/ns-ntsecpkg-_secpkg_function_table">SECPKG_FUNCTION_TABLE</a> structure received from the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-splsamodeinitializefn">SpLsaModeInitialize</a> function.

A pointer to the user-mode implementation of the <b>SpQueryContextAttributes</b> function is available in the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/ns-ntsecpkg-_secpkg_user_function_table">SECPKG_USER_FUNCTION_TABLE</a> structure received from the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spusermodeinitializefn">SpUserModeInitialize</a> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/ns-ntsecpkg-_secpkg_function_table">SECPKG_FUNCTION_TABLE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-splsamodeinitializefn">SpLsaModeInitialize</a>
 

 


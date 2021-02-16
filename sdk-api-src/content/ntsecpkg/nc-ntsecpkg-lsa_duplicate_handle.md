---
UID: NC:ntsecpkg.LSA_DUPLICATE_HANDLE
title: LSA_DUPLICATE_HANDLE (ntsecpkg.h)
description: The DuplicateHandle function creates a duplicate handle. The returned duplicate is in the caller's process space.
helpviewer_keywords: ["DuplicateHandle","DuplicateHandle callback function [Security]","LSA_DUPLICATE_HANDLE","LSA_DUPLICATE_HANDLE callback","_ssp_duplicatehandle","ntsecpkg/DuplicateHandle","security.duplicatehandle"]
old-location: security\duplicatehandle.htm
tech.root: security
ms.assetid: 1930a33c-2921-4ac1-994a-ee4686d6a66b
ms.date: 12/05/2018
ms.keywords: DuplicateHandle, DuplicateHandle callback function [Security], LSA_DUPLICATE_HANDLE, LSA_DUPLICATE_HANDLE callback, _ssp_duplicatehandle, ntsecpkg/DuplicateHandle, security.duplicatehandle
req.header: ntsecpkg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - LSA_DUPLICATE_HANDLE
 - ntsecpkg/LSA_DUPLICATE_HANDLE
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
 - DuplicateHandle
---

# LSA_DUPLICATE_HANDLE callback function


## -description

The <b>DuplicateHandle</b> function creates a duplicate handle. The returned duplicate is in the caller's process space.

## -parameters

### -param SourceHandle [in]

A handle to duplicate.

### -param DestionationHandle [out]

Pointer that receives the address of a duplicate of the <i>SourceHandle</i> handle. The duplicate handle is in the caller's process space. When you have finished using the handle, close it by calling the <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function.

## -returns

If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code indicating the reason it failed.

## -remarks

A pointer to the <b>DuplicateHandle</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a>
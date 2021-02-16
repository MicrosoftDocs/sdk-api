---
UID: NS:ntsecpkg._LSA_DISPATCH_TABLE
title: LSA_DISPATCH_TABLE (ntsecpkg.h)
description: Contains pointers to the Local Security Authority (LSA) functions that Windows authentication packages can call.
helpviewer_keywords: ["*PLSA_DISPATCH_TABLE","LSA_DISPATCH_TABLE","LSA_DISPATCH_TABLE structure [Security]","PLSA_DISPATCH_TABLE","PLSA_DISPATCH_TABLE structure pointer [Security]","_LSA_DISPATCH_TABLE","_lsa_lsa_dispatch_table","ntsecpkg/LSA_DISPATCH_TABLE","ntsecpkg/PLSA_DISPATCH_TABLE","security.lsa_dispatch_table"]
old-location: security\lsa_dispatch_table.htm
tech.root: security
ms.assetid: 2e144ce0-e8c9-457a-8b12-7d21dda6adf3
ms.date: 12/05/2018
ms.keywords: '*PLSA_DISPATCH_TABLE, LSA_DISPATCH_TABLE, LSA_DISPATCH_TABLE structure [Security], PLSA_DISPATCH_TABLE, PLSA_DISPATCH_TABLE structure pointer [Security], _LSA_DISPATCH_TABLE, _lsa_lsa_dispatch_table, ntsecpkg/LSA_DISPATCH_TABLE, ntsecpkg/PLSA_DISPATCH_TABLE, security.lsa_dispatch_table'
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
req.typenames: LSA_DISPATCH_TABLE, *PLSA_DISPATCH_TABLE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _LSA_DISPATCH_TABLE
 - ntsecpkg/_LSA_DISPATCH_TABLE
 - PLSA_DISPATCH_TABLE
 - ntsecpkg/PLSA_DISPATCH_TABLE
 - LSA_DISPATCH_TABLE
 - ntsecpkg/LSA_DISPATCH_TABLE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecpkg.h
api_name:
 - LSA_DISPATCH_TABLE
---

# LSA_DISPATCH_TABLE structure


## -description

The <b>LSA_DISPATCH_TABLE</b> structure contains pointers to the <a href="/windows/desktop/SecGloss/l-gly">Local Security Authority</a> (LSA) functions that Windows <a href="/windows/desktop/SecGloss/a-gly">authentication packages</a> can call.

The LSA passes this structure to an authentication package when it calls the  
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_ap_initialize_package">LsaApInitializePackage</a> function of the package.

## -struct-fields

### -field CreateLogonSession

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_create_logon_session">CreateLogonSession</a> function.

### -field DeleteLogonSession

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_delete_logon_session">DeleteLogonSession</a> function.

### -field AddCredential

Pointer to the 
					<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_add_credential">AddCredential</a> function.

### -field GetCredentials

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_get_credentials">GetCredentials</a> function.

### -field DeleteCredential

Pointer to the
					<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_delete_credential">DeleteCredential</a> function.

### -field AllocateLsaHeap

Pointer to the
					<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_allocate_lsa_heap">AllocateLsaHeap</a> function.

### -field FreeLsaHeap

Pointer to the
					<a href="/windows/desktop/api/ntlsa/nc-ntlsa-lsa_free_lsa_heap">FreeLsaHeap</a> function.

### -field AllocateClientBuffer

Pointer to the
					<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_allocate_client_buffer">AllocateClientBuffer</a> function.

### -field FreeClientBuffer

Pointer to the
					<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_free_client_buffer">FreeClientBuffer</a> function.

### -field CopyToClientBuffer

Pointer to the
					<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_copy_to_client_buffer">CopyToClientBuffer</a>  function.

### -field CopyFromClientBuffer

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_copy_from_client_buffer">CopyFromClientBuffer</a> function.
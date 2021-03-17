---
UID: NS:ntsecpkg._LSA_SECPKG_FUNCTION_TABLE
title: LSA_SECPKG_FUNCTION_TABLE (ntsecpkg.h)
description: Contains pointers to the LSA functions that a security package can call. The Local Security Authority (LSA) passes this structure to a security package when it calls the package's SpInitialize function.
helpviewer_keywords: ["*PLSA_SECPKG_FUNCTION_TABLE","LSA_SECPKG_FUNCTION_TABLE","LSA_SECPKG_FUNCTION_TABLE structure [Security]","PLSA_SECPKG_FUNCTION_TABLE","PLSA_SECPKG_FUNCTION_TABLE structure pointer [Security]","_ssp_lsa_secpkg_function_table","ntsecpkg/LSA_SECPKG_FUNCTION_TABLE","ntsecpkg/PLSA_SECPKG_FUNCTION_TABLE","security.lsa_secpkg_function_table"]
old-location: security\lsa_secpkg_function_table.htm
tech.root: security
ms.assetid: 85f04072-8634-454a-9038-737d86c5597d
ms.date: 12/05/2018
ms.keywords: '*PLSA_SECPKG_FUNCTION_TABLE, LSA_SECPKG_FUNCTION_TABLE, LSA_SECPKG_FUNCTION_TABLE structure [Security], PLSA_SECPKG_FUNCTION_TABLE, PLSA_SECPKG_FUNCTION_TABLE structure pointer [Security], _ssp_lsa_secpkg_function_table, ntsecpkg/LSA_SECPKG_FUNCTION_TABLE, ntsecpkg/PLSA_SECPKG_FUNCTION_TABLE, security.lsa_secpkg_function_table'
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
req.typenames: LSA_SECPKG_FUNCTION_TABLE, *PLSA_SECPKG_FUNCTION_TABLE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _LSA_SECPKG_FUNCTION_TABLE
 - ntsecpkg/_LSA_SECPKG_FUNCTION_TABLE
 - PLSA_SECPKG_FUNCTION_TABLE
 - ntsecpkg/PLSA_SECPKG_FUNCTION_TABLE
 - LSA_SECPKG_FUNCTION_TABLE
 - ntsecpkg/LSA_SECPKG_FUNCTION_TABLE
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
 - LSA_SECPKG_FUNCTION_TABLE
---

# LSA_SECPKG_FUNCTION_TABLE structure


## -description

The <b>LSA_SECPKG_FUNCTION_TABLE</b> structure contains pointers to the LSA functions that a <a href="/windows/desktop/SecGloss/s-gly">security package</a> can call. The <a href="/windows/desktop/SecGloss/l-gly">Local Security Authority</a> (LSA) passes this structure to a security package when it calls the package's 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a> function.

## -struct-fields

### -field CreateLogonSession

Pointer to the  <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_create_logon_session">CreateLogonSession</a> function.

### -field DeleteLogonSession

Pointer to the  <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_delete_logon_session">DeleteLogonSession</a> function.

### -field AddCredential

Pointer to the  <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_add_credential">AddCredential</a> function.

### -field GetCredentials

Pointer to the  <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_get_credentials">GetCredentials</a> function.

### -field DeleteCredential

Pointer to the  <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_delete_credential">DeleteCredential</a> function.

### -field AllocateLsaHeap

Pointer to the  <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_allocate_lsa_heap">AllocateLsaHeap</a> function.

### -field FreeLsaHeap

Pointer to the  <a href="/windows/desktop/api/ntlsa/nc-ntlsa-lsa_free_lsa_heap">FreeLsaHeap</a> function.

### -field AllocateClientBuffer

Pointer to the  <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_allocate_client_buffer">AllocateClientBuffer</a> function.

### -field FreeClientBuffer

Pointer to the  <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_free_client_buffer">FreeClientBuffer</a> function.

### -field CopyToClientBuffer

Pointer to the  <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_copy_to_client_buffer">CopyToClientBuffer</a> function.

### -field CopyFromClientBuffer

Pointer to the  <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_copy_from_client_buffer">CopyFromClientBuffer</a> function.

### -field ImpersonateClient

Pointer to the  <a href="/previous-versions/windows/desktop/legacy/aa375494(v=vs.85)">ImpersonateClient</a> function.

### -field UnloadPackage

Pointer to the  <a href="/previous-versions/windows/desktop/legacy/aa380520(v=vs.85)">UnloadPackage</a> function.

### -field DuplicateHandle

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_duplicate_handle">DuplicateHandle</a>  function.

### -field SaveSupplementalCredentials

Pointer to the <b>SaveSupplementalCredentials</b>  function.

### -field CreateThread

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_create_thread">CreateThread</a>  function.

### -field GetClientInfo

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_get_client_info">GetClientInfo</a>  function.

### -field RegisterNotification

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_register_notification">RegisterNotification</a>  function.

### -field CancelNotification

Pointer to the  <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_cancel_notification">CancelNotification</a> function.

### -field MapBuffer

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_map_buffer">MapBuffer</a>  function.

### -field CreateToken

Pointer to the  <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_create_token">CreateToken</a> function.

### -field AuditLogon

Pointer to the   <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_audit_logon">AuditLogon</a> function.

### -field CallPackage

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_call_package">CallPackage</a>  function.

### -field FreeReturnBuffer

Pointer to the  <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_free_lsa_heap">FreeReturnBuffer</a> function.

### -field GetCallInfo

Pointer to the  <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_get_call_info">GetCallInfo</a> function.

### -field CallPackageEx

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_call_packageex">CallPackageEx</a>  function.

### -field CreateSharedMemory

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_create_shared_memory">CreateSharedMemory</a>  function.

### -field AllocateSharedMemory

Pointer to the   <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_allocate_shared_memory">AllocateSharedMemory</a> function.

### -field FreeSharedMemory

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_free_shared_memory">FreeSharedMemory</a>  function.

### -field DeleteSharedMemory

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_delete_shared_memory">DeleteSharedMemory</a>  function.

### -field OpenSamUser

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_open_sam_user">OpenSamUser</a>  function.

### -field GetUserCredentials

Pointer to the  <b>GetUserCredentials</b> function.

### -field GetUserAuthData

Pointer to the  <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_get_user_auth_data">GetUserAuthData</a> function.

### -field CloseSamUser

Pointer to the  <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_close_sam_user">CloseSamUser</a> function.

### -field ConvertAuthDataToToken

Pointer to the  <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_convert_auth_data_to_token">ConvertAuthDataToToken</a> function.

### -field ClientCallback

Pointer to the  <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_client_callback">ClientCallback</a> function.

### -field UpdateCredentials

Pointer to the  <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_update_primary_credentials">UpdateCredentials</a> function.

### -field GetAuthDataForUser

Pointer to the  <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_get_auth_data_for_user">GetAuthDataForUser</a> function.

### -field CrackSingleName

Pointer to the  <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_crack_single_name">CrackSingleName</a> function.

### -field AuditAccountLogon

Pointer to the  <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_audit_account_logon">AuditAccountLogon</a> function.

### -field CallPackagePassthrough

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_call_package_passthrough">CallPackagePassthrough</a> function.

### -field CrediRead

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-credreadfn">CrediRead</a> function.

### -field CrediReadDomainCredentials

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-credreaddomaincredentialsfn">CrediReadDomainCredentials</a> function.

### -field CrediFreeCredentials

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-credfreecredentialsfn">CrediFreeCredentials</a> function.

### -field DummyFunction1

### -field DummyFunction2

### -field DummyFunction3

### -field LsaProtectMemory

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_protect_memory">LsaProtectMemory</a> function.

### -field LsaUnprotectMemory

Pointer to the <a href="/previous-versions/windows/desktop/legacy/ff714510(v=vs.85)">LsaUnprotectMemory</a> function.

### -field OpenTokenByLogonId

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_open_token_by_logon_id">OpenTokenByLogonId</a> function.

### -field ExpandAuthDataForDomain

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_expand_auth_data_for_domain">ExpandAuthDataForDomain</a> function.

### -field AllocatePrivateHeap

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_allocate_private_heap">AllocatePrivateHeap</a> function.

### -field FreePrivateHeap

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_free_private_heap">FreePrivateHeap</a> function.

### -field CreateTokenEx

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_create_token_ex">CreateTokenEx</a> function.

### -field CrediWrite

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-credwritefn">CrediWrite</a> function.

### -field CrediUnmarshalandDecodeString

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-crediunmarshalanddecodestringfn">CrediUnmarshalandDecodeString</a> function.

<b>Windows Server 2003 and Windows XP:  </b>This function is not implemented.

### -field DummyFunction4

### -field DummyFunction5

### -field DummyFunction6

Introduced in Windows 8 and above for internal Microsoft use only.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This function is not implemented.

### -field GetExtendedCallFlags

Pointer to the <b>GetExtendedCallFlags</b> function.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This function is not implemented.

### -field DuplicateTokenHandle

Pointer to the <b>DuplicateTokenHandle</b> function.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This function is not implemented.

### -field GetServiceAccountPassword

Pointer to the <b>GetServiceAccountPassword</b> function.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This function is not implemented.

### -field DummyFunction7

Introduced in Windows 8 and above for internal Microsoft use only.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This function is not implemented.

### -field AuditLogonEx

Pointer to the <b>AuditLogonEx</b> function.

### -field CheckProtectedUserByToken

Pointer to the <b>CheckProtectedUserByToken</b> function.

### -field QueryClientRequest

Pointer to the <b>QueryClientRequest</b> function.

### -field GetAppModeInfo

Pointer to the <b>GetAppModeInfo</b> function.

### -field SetAppModeInfo

Pointer to the <b>SetAppModeInfo</b> function.
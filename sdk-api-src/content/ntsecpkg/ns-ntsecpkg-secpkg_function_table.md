---
UID: NS:ntsecpkg._SECPKG_FUNCTION_TABLE
title: SECPKG_FUNCTION_TABLE (ntsecpkg.h)
description: The SECPKG_FUNCTION_TABLE structure contains pointers to the LSA functions that a security package must implement. The Local Security Authority (LSA) obtains this structure from an SSP/AP DLL when it calls the SpLsaModeInitialize function.
helpviewer_keywords: ["*PSECPKG_FUNCTION_TABLE","PSECPKG_FUNCTION_TABLE","PSECPKG_FUNCTION_TABLE structure pointer [Security]","SECPKG_FUNCTION_TABLE","SECPKG_FUNCTION_TABLE structure [Security]","_ssp_secpkg_function_table","ntsecpkg/PSECPKG_FUNCTION_TABLE","ntsecpkg/SECPKG_FUNCTION_TABLE","security.secpkg_function_table"]
old-location: security\secpkg_function_table.htm
tech.root: security
ms.assetid: 43ca0f9b-1393-48aa-9d9c-4dd19963a66d
ms.date: 12/05/2018
ms.keywords: '*PSECPKG_FUNCTION_TABLE, PSECPKG_FUNCTION_TABLE, PSECPKG_FUNCTION_TABLE structure pointer [Security], SECPKG_FUNCTION_TABLE, SECPKG_FUNCTION_TABLE structure [Security], _ssp_secpkg_function_table, ntsecpkg/PSECPKG_FUNCTION_TABLE, ntsecpkg/SECPKG_FUNCTION_TABLE, security.secpkg_function_table'
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
req.typenames: SECPKG_FUNCTION_TABLE, *PSECPKG_FUNCTION_TABLE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SECPKG_FUNCTION_TABLE
 - ntsecpkg/_SECPKG_FUNCTION_TABLE
 - PSECPKG_FUNCTION_TABLE
 - ntsecpkg/PSECPKG_FUNCTION_TABLE
 - SECPKG_FUNCTION_TABLE
 - ntsecpkg/SECPKG_FUNCTION_TABLE
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
 - SECPKG_FUNCTION_TABLE
---

# SECPKG_FUNCTION_TABLE structure


## -description

The <b>SECPKG_FUNCTION_TABLE</b> structure contains pointers to the LSA functions that a <a href="/windows/desktop/SecGloss/s-gly">security package</a> must implement. The <a href="/windows/desktop/SecGloss/l-gly">Local Security Authority</a> (LSA) obtains this structure from an SSP/AP DLL when it calls the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-splsamodeinitializefn">SpLsaModeInitialize</a> function.

## -struct-fields

### -field InitializePackage

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_ap_initialize_package">LsaApInitializePackage</a> function.

### -field LogonUser

Pointer to the <a href="/windows/desktop/api/winbase/nf-winbase-logonusera">LogonUser</a> function.

### -field CallPackage

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_call_package">CallPackage</a> function.

### -field LogonTerminated

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_ap_logon_terminated">LsaApLogonTerminated</a> function.

### -field CallPackageUntrusted

Pointer to the <a href="/previous-versions/windows/desktop/legacy/aa378218(v=vs.85)">LsaApCallPackageUntrusted</a>  function.

### -field CallPackagePassthrough

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_call_package_passthrough">CallPackagePassthrough</a> function.

### -field LogonUserEx

Pointer to the <a href="/windows/desktop/api/winbase/nf-winbase-logonuserexa">LogonUserEx</a> function.

### -field LogonUserEx2

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_ap_logon_user_ex2">LsaApLogonUserEx2</a> function.

### -field Initialize

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a> function.

### -field Shutdown

Pointer to the <a href="/previous-versions/windows/desktop/legacy/aa380183(v=vs.85)">SpShutdown</a> function.

### -field GetInfo

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spgetinfofn">SpGetInfo</a> function.

### -field AcceptCredentials

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spacceptcredentialsfn">SpAcceptCredentials</a> function.

### -field AcquireCredentialsHandle

Pointer to the <a href="/windows/desktop/api/sspi/nf-sspi-acquirecredentialshandlea">AcquireCredentialsHandle</a> function.

### -field QueryCredentialsAttributes

Pointer to the <a href="/windows/desktop/api/sspi/nf-sspi-querycredentialsattributesa">QueryCredentialsAttributes</a> function.

### -field FreeCredentialsHandle

Pointer to the <a href="/windows/desktop/api/sspi/nf-sspi-freecredentialshandle">FreeCredentialsHandle</a> function.

### -field SaveCredentials

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spsavecredentialsfn">SpSaveCredentials</a> function.

### -field GetCredentials

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_get_credentials">GetCredentials</a> function.

### -field DeleteCredentials

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spdeletecredentialsfn">SpDeleteCredentials</a> function.

### -field InitLsaModeContext

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitlsamodecontextfn">SpInitLsaModeContext</a> function.

### -field AcceptLsaModeContext

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spacceptlsamodecontextfn">SpAcceptLsaModeContext</a> function.

### -field DeleteContext

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-kspdeletecontextfn">SpDeleteContext</a> function.

### -field ApplyControlToken

Pointer to the <a href="/windows/desktop/api/sspi/nf-sspi-applycontroltoken">ApplyControlToken</a> function.

### -field GetUserInfo

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spgetuserinfofn">SpGetUserInfo</a> function.

### -field GetExtendedInformation

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spgetextendedinformationfn">SpGetExtendedInformation
</a> function.

### -field QueryContextAttributes

Pointer to the <a href="/windows/desktop/api/sspi/nf-sspi-querycontextattributesa">QueryContextAttributes (General)</a> function.

### -field AddCredentials

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spaddcredentialsfn">SpAddCredentials</a> function.

### -field SetExtendedInformation

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spsetextendedinformationfn">SpSetExtendedInformation</a> function.

### -field SetContextAttributes

Pointer to the <a href="/windows/desktop/api/sspi/nf-sspi-setcontextattributesa">SetContextAttributes</a> function.

### -field SetCredentialsAttributes

Pointer to the <a href="/windows/desktop/api/sspi/nf-sspi-setcredentialsattributesa">SetCredentialsAttributes</a> function.

### -field ChangeAccountPassword

Pointer to the <a href="/windows/desktop/api/sspi/nf-sspi-changeaccountpassworda">ChangeAccountPassword</a> function.

### -field QueryMetaData

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spquerymetadatafn">QueryMetaData</a> function.

### -field ExchangeMetaData

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spexchangemetadatafn">ExchangeMetaData</a> function.

### -field GetCredUIContext

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spgetcreduicontextfn">GetCredUIContext</a> function.

### -field UpdateCredentials

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spupdatecredentialsfn">UpdateCredentials</a> function.

### -field ValidateTargetInfo

Pointer to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spvalidatetargetinfofn">SpValidateTargetInfoFn</a> function.

### -field PostLogonUser

### -field GetRemoteCredGuardLogonBuffer

### -field GetRemoteCredGuardSupplementalCreds

### -field GetTbalSupplementalCreds

### -field LogonUserEx3

### -field PreLogonUserSurrogate

### -field PostLogonUserSurrogate

### -field ExtractTargetInfo

 

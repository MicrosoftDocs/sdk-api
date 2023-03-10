---
UID: NS:ntsecpkg._SECPKG_USER_FUNCTION_TABLE
title: SECPKG_USER_FUNCTION_TABLE (ntsecpkg.h)
description: The SECPKG_USER_FUNCTION_TABLE structure contains pointers to the functions that a security package implements to support executing in process with client/server applications. This structure is provided by the SpUserModeInitialize function.
helpviewer_keywords: ["*PSECPKG_USER_FUNCTION_TABLE","PSECPKG_USER_FUNCTION_TABLE","PSECPKG_USER_FUNCTION_TABLE structure pointer [Security]","SECPKG_USER_FUNCTION_TABLE","SECPKG_USER_FUNCTION_TABLE structure [Security]","_ssp_secpkg_user_function_table","ntsecpkg/PSECPKG_USER_FUNCTION_TABLE","ntsecpkg/SECPKG_USER_FUNCTION_TABLE","security.secpkg_user_function_table"]
old-location: security\secpkg_user_function_table.htm
tech.root: security
ms.assetid: 2b3fc6d1-2f55-4053-9271-f5cb5c318555
ms.date: 12/05/2018
ms.keywords: '*PSECPKG_USER_FUNCTION_TABLE, PSECPKG_USER_FUNCTION_TABLE, PSECPKG_USER_FUNCTION_TABLE structure pointer [Security], SECPKG_USER_FUNCTION_TABLE, SECPKG_USER_FUNCTION_TABLE structure [Security], _ssp_secpkg_user_function_table, ntsecpkg/PSECPKG_USER_FUNCTION_TABLE, ntsecpkg/SECPKG_USER_FUNCTION_TABLE, security.secpkg_user_function_table'
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
req.typenames: SECPKG_USER_FUNCTION_TABLE, *PSECPKG_USER_FUNCTION_TABLE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SECPKG_USER_FUNCTION_TABLE
 - ntsecpkg/_SECPKG_USER_FUNCTION_TABLE
 - PSECPKG_USER_FUNCTION_TABLE
 - ntsecpkg/PSECPKG_USER_FUNCTION_TABLE
 - SECPKG_USER_FUNCTION_TABLE
 - ntsecpkg/SECPKG_USER_FUNCTION_TABLE
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
 - SECPKG_USER_FUNCTION_TABLE
---

# SECPKG_USER_FUNCTION_TABLE structure


## -description

The <b>SECPKG_USER_FUNCTION_TABLE</b> structure contains pointers to the functions that a <a href="/windows/desktop/SecGloss/s-gly">security package</a> implements to support executing in process with client/server applications. This structure is provided by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spusermodeinitializefn">SpUserModeInitialize</a> function.

## -struct-fields

### -field InstanceInit

Pointer to the <b>InstanceInit</b> function.

### -field InitUserModeContext

Pointer to the <b>InitUserModeContext</b> function.

### -field MakeSignature

Pointer to the <a href="/windows/desktop/api/sspi/nf-sspi-makesignature">MakeSignature</a> function.

### -field VerifySignature

Pointer to the <a href="/windows/desktop/api/sspi/nf-sspi-verifysignature">VerifySignature</a> function.

### -field SealMessage

Pointer to the <b>SealMessage</b> function.

### -field UnsealMessage

Pointer to the <b>UnsealMessage</b> function.

### -field GetContextToken

Pointer to the <b>GetContextToken</b> function.

### -field QueryContextAttributes

Pointer to the <a href="/windows/desktop/api/sspi/nf-sspi-querycontextattributesa">QueryContextAttributes (General)</a> function.

### -field CompleteAuthToken

Pointer to the <a href="/windows/desktop/api/sspi/nf-sspi-completeauthtoken">CompleteAuthToken</a> function.

### -field DeleteUserModeContext

Pointer to the <b>DeleteUserModeContext</b> function.

### -field FormatCredentials

Pointer to the <b>FormatCredentials</b> function.

### -field MarshallSupplementalCreds

Pointer to the <b>MarshallSupplementalCreds</b> function.

### -field ExportContext

Pointer to the <b>ExportContext</b> function.

### -field ImportContext

Pointer to the <b>ImportContext</b> function.
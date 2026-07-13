---
UID: NS:sspi._SECURITY_FUNCTION_TABLE_W
title: SecurityFunctionTableW (sspi.h)
description: The SecurityFunctionTable structure is a dispatch table that contains pointers to the functions defined in SSPI. (Unicode)
helpviewer_keywords: ["*PSecurityFunctionTableW","PSecurityFunctionTable","PSecurityFunctionTable structure pointer [Security]","SECURITY_SUPPORT_PROVIDER_INTERFACE_VERSION","SECURITY_SUPPORT_PROVIDER_INTERFACE_VERSION structure [Security]","SecurityFunctionTable","SecurityFunctionTable structure [Security]","SecurityFunctionTableA","SecurityFunctionTableW","_ssp_securityfunctiontable","security.securityfunctiontable","sspi/PSecurityFunctionTable","sspi/SECURITY_SUPPORT_PROVIDER_INTERFACE_VERSION","sspi/SecurityFunctionTable","sspi/SecurityFunctionTableA","sspi/SecurityFunctionTableW"]
old-location: security\securityfunctiontable.htm
tech.root: security
ms.assetid: 6315e8d6-b40a-4dd6-b6a6-598a965f93dc
ms.date: 12/05/2018
ms.keywords: '*PSecurityFunctionTableW, PSecurityFunctionTable, PSecurityFunctionTable structure pointer [Security], SECURITY_SUPPORT_PROVIDER_INTERFACE_VERSION, SECURITY_SUPPORT_PROVIDER_INTERFACE_VERSION structure [Security], SecurityFunctionTable, SecurityFunctionTable structure [Security], SecurityFunctionTableA, SecurityFunctionTableW, _ssp_securityfunctiontable, security.securityfunctiontable, sspi/PSecurityFunctionTable, sspi/SECURITY_SUPPORT_PROVIDER_INTERFACE_VERSION, sspi/SecurityFunctionTable, sspi/SecurityFunctionTableA, sspi/SecurityFunctionTableW'
req.header: sspi.h
req.include-header: Security.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SecurityFunctionTableW (Unicode) and SecurityFunctionTableA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SecurityFunctionTableW, *PSecurityFunctionTableW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SECURITY_FUNCTION_TABLE_W
 - sspi/_SECURITY_FUNCTION_TABLE_W
 - PSecurityFunctionTableW
 - sspi/PSecurityFunctionTableW
 - SecurityFunctionTableW
 - sspi/SecurityFunctionTableW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Sspi.h
api_name:
 - SecurityFunctionTable
 - SecurityFunctionTableA
 - SecurityFunctionTableW
---

# SecurityFunctionTableW structure


## -description

The <b>SecurityFunctionTable</b> structure is a dispatch table that contains pointers to the functions defined in SSPI.

## -struct-fields

### -field dwVersion

Version number of the table.

### -field EnumerateSecurityPackagesW

### -field QueryCredentialsAttributesW

### -field AcquireCredentialsHandleW

### -field FreeCredentialsHandle

Pointer to the <a href="/windows/desktop/api/sspi/nf-sspi-freecredentialshandle">FreeCredentialsHandle</a> function.

### -field Reserved2

Reserved for future use.

### -field InitializeSecurityContextW

### -field AcceptSecurityContext

Pointer to the <a href="/windows/desktop/api/sspi/nf-sspi-acceptsecuritycontext">AcceptSecurityContext (General)</a> function.

### -field CompleteAuthToken

Pointer to the <a href="/windows/desktop/api/sspi/nf-sspi-completeauthtoken">CompleteAuthToken</a> function.

### -field DeleteSecurityContext

Pointer to the <a href="/windows/desktop/api/sspi/nf-sspi-deletesecuritycontext">DeleteSecurityContext</a> function.

### -field ApplyControlToken

Pointer to the <a href="/windows/desktop/api/sspi/nf-sspi-applycontroltoken">ApplyControlToken</a> function.

### -field QueryContextAttributesW

### -field ImpersonateSecurityContext

Pointer to the <a href="/windows/desktop/api/sspi/nf-sspi-impersonatesecuritycontext">ImpersonateSecurityContext</a> function.

### -field RevertSecurityContext

Pointer to the <a href="/windows/desktop/api/sspi/nf-sspi-revertsecuritycontext">RevertSecurityContext</a> function.

### -field MakeSignature

Pointer to the <a href="/windows/desktop/api/sspi/nf-sspi-makesignature">MakeSignature</a> function.

### -field VerifySignature

Pointer to the <a href="/windows/desktop/api/sspi/nf-sspi-verifysignature">VerifySignature</a> function.

### -field FreeContextBuffer

Pointer to the <a href="/windows/desktop/api/sspi/nf-sspi-freecontextbuffer">FreeContextBuffer</a> function.

### -field QuerySecurityPackageInfoW

### -field Reserved3

Reserved for future use.

### -field Reserved4

Reserved for future use.

### -field ExportSecurityContext

Pointer to the <a href="/windows/desktop/api/sspi/nf-sspi-exportsecuritycontext">ExportSecurityContext</a> function.

### -field ImportSecurityContextW

### -field AddCredentialsW

### -field Reserved8

Reserved for future use.

### -field QuerySecurityContextToken

Pointer to the  <a href="/windows/desktop/api/sspi/nf-sspi-querysecuritycontexttoken">QuerySecurityContextToken</a> function.

### -field EncryptMessage

Pointer to the  <a href="/windows/desktop/api/sspi/nf-sspi-encryptmessage">EncryptMessage (General)</a> function.

### -field DecryptMessage

Pointer to the   <a href="/windows/desktop/api/sspi/nf-sspi-decryptmessage">DecryptMessage (General)</a> function.

### -field SetContextAttributesW

### -field SetCredentialsAttributesW

### -field ChangeAccountPasswordW

### -field Reserved9

### -field QueryContextAttributesExW

### -field QueryCredentialsAttributesExW

 




#### - AcquireCredentialsHandle

Pointer to the <a href="/windows/desktop/api/sspi/nf-sspi-acquirecredentialshandlea">AcquireCredentialsHandle</a> function.


#### - AddCredentials

Pointer to the  <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_add_credential">AddCredential</a> function.


#### - EnumerateSecurityPackages

Pointer to the <a href="/windows/desktop/api/sspi/nf-sspi-enumeratesecuritypackagesa">EnumerateSecurityPackages</a> function.


#### - ImportSecurityContext

Pointer to the <a href="/windows/desktop/api/sspi/nf-sspi-importsecuritycontexta">ImportSecurityContext</a> function.


#### - InitializeSecurityContext

Pointer to the  <a href="/windows/desktop/api/sspi/nf-sspi-initializesecuritycontexta">InitializeSecurityContext (General)</a> function.


#### - QueryContextAttributes

Pointer to the  <a href="/windows/desktop/api/sspi/nf-sspi-querycontextattributesa">QueryContextAttributes (General)</a> function.


#### - QueryCredentialsAttributes

Pointer to the  <a href="/windows/desktop/api/sspi/nf-sspi-querycredentialsattributesa">QueryCredentialsAttributes</a> function.


#### - QuerySecurityPackageInfo

Pointer to the   <a href="/windows/desktop/api/sspi/nf-sspi-querysecuritypackageinfoa">QuerySecurityPackageInfo</a> function.


#### - Reserved1

Reserved for future use.


#### - SetContextAttributes

Pointer to the   <a href="/windows/desktop/api/sspi/nf-sspi-setcontextattributesa">SetContextAttributes</a> function.

## -see-also

<a href="/windows/desktop/api/sspi/nf-sspi-initsecurityinterfacea">InitSecurityInterface</a>

## -remarks

> [!NOTE]
> The sspi.h header defines SecurityFunctionTable as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

QueryContextAttributesExW and QueryCredentialsAttributesW are not initialized.

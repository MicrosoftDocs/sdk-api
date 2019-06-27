---
UID: NS:sspi._SECURITY_FUNCTION_TABLE_A
title: SecurityFunctionTableA (sspi.h)
author: windows-sdk-content
description: The SecurityFunctionTable structure is a dispatch table that contains pointers to the functions defined in SSPI.
old-location: security\securityfunctiontable.htm
tech.root: SecAuthN
ms.assetid: 6315e8d6-b40a-4dd6-b6a6-598a965f93dc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PSecurityFunctionTableA, PSecurityFunctionTable, PSecurityFunctionTable structure pointer [Security], SECURITY_SUPPORT_PROVIDER_INTERFACE_VERSION, SECURITY_SUPPORT_PROVIDER_INTERFACE_VERSION structure [Security], SecurityFunctionTable, SecurityFunctionTable structure [Security], SecurityFunctionTableA, SecurityFunctionTableW, _ssp_securityfunctiontable, security.securityfunctiontable, sspi/PSecurityFunctionTable, sspi/SECURITY_SUPPORT_PROVIDER_INTERFACE_VERSION, sspi/SecurityFunctionTable, sspi/SecurityFunctionTableA, sspi/SecurityFunctionTableW"
ms.topic: struct
f1_keywords: 
 - "sspi/SecurityFunctionTable"
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
product: Windows
targetos: Windows
req.typenames: SecurityFunctionTableA, *PSecurityFunctionTableA
req.redist: 
ms.custom: 19H1
---

# SecurityFunctionTableA structure


## -description


The <b>SecurityFunctionTable</b> structure is a dispatch table that contains pointers to the functions defined in SSPI.


## -struct-fields




### -field dwVersion

Version number of the table.


### -field EnumerateSecurityPackagesA

 


### -field QueryCredentialsAttributesA

 


### -field AcquireCredentialsHandleA

 


### -field FreeCredentialHandle

 


### -field Reserved2

Reserved for future use.


### -field InitializeSecurityContextA

 


### -field AcceptSecurityContext

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/sspi/nf-sspi-acceptsecuritycontext">AcceptSecurityContext (General)</a> function.


### -field CompleteAuthToken

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/sspi/nf-sspi-completeauthtoken">CompleteAuthToken</a> function.


### -field DeleteSecurityContext

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/sspi/nf-sspi-deletesecuritycontext">DeleteSecurityContext</a> function.


### -field ApplyControlToken

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/sspi/nf-sspi-applycontroltoken">ApplyControlToken</a> function.


### -field QueryContextAttributesA

 


### -field ImpersonateSecurityContext

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/sspi/nf-sspi-impersonatesecuritycontext">ImpersonateSecurityContext</a> function.


### -field RevertSecurityContext

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/sspi/nf-sspi-revertsecuritycontext">RevertSecurityContext</a> function.


### -field MakeSignature

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/sspi/nf-sspi-makesignature">MakeSignature</a> function.


### -field VerifySignature

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/sspi/nf-sspi-verifysignature">VerifySignature</a> function.


### -field FreeContextBuffer

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/sspi/nf-sspi-freecontextbuffer">FreeContextBuffer</a> function.


### -field QuerySecurityPackageInfoA

 


### -field Reserved3

Reserved for future use.


### -field Reserved4

Reserved for future use.


### -field ExportSecurityContext

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/sspi/nf-sspi-exportsecuritycontext">ExportSecurityContext</a> function.


### -field ImportSecurityContextA

 


### -field AddCredentialsA

 


### -field Reserved8

Reserved for future use.


### -field QuerySecurityContextToken

Pointer to the  <a href="https://docs.microsoft.com/windows/desktop/api/sspi/nf-sspi-querysecuritycontexttoken">QuerySecurityContextToken</a> function.


### -field EncryptMessage

Pointer to the  <a href="https://docs.microsoft.com/windows/desktop/api/sspi/nf-sspi-encryptmessage">EncryptMessage (General)</a> function.


### -field DecryptMessage

Pointer to the   <a href="https://docs.microsoft.com/windows/desktop/api/sspi/nf-sspi-decryptmessage">DecryptMessage (General)</a> function.


### -field SetContextAttributesA

 


### -field SetCredentialsAttributesA

 


### -field ChangeAccountPasswordA

 


### -field Reserved9

 


### -field QueryContextAttributesExA

 


### -field QueryCredentialsAttributesExA

 




#### - AcquireCredentialsHandle

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/sspi/nf-sspi-acquirecredentialshandlea">AcquireCredentialsHandle</a> function.


#### - AddCredentials

Pointer to the  <a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_add_credential">AddCredential</a> function.


#### - EnumerateSecurityPackages

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/sspi/nf-sspi-enumeratesecuritypackagesa">EnumerateSecurityPackages</a> function.


#### - FreeCredentialsHandle

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/sspi/nf-sspi-freecredentialshandle">FreeCredentialsHandle</a> function.


#### - ImportSecurityContext

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/sspi/nf-sspi-importsecuritycontexta">ImportSecurityContext</a> function.


#### - InitializeSecurityContext

Pointer to the  <a href="https://docs.microsoft.com/windows/desktop/api/sspi/nf-sspi-initializesecuritycontexta">InitializeSecurityContext (General)</a> function.


#### - QueryContextAttributes

Pointer to the  <a href="https://docs.microsoft.com/windows/desktop/api/sspi/nf-sspi-querycontextattributesa">QueryContextAttributes (General)</a> function.


#### - QueryCredentialsAttributes

Pointer to the  <a href="https://docs.microsoft.com/windows/desktop/api/sspi/nf-sspi-querycredentialsattributesa">QueryCredentialsAttributes</a> function.


#### - QuerySecurityPackageInfo

Pointer to the   <a href="https://docs.microsoft.com/windows/desktop/api/sspi/nf-sspi-querysecuritypackageinfoa">QuerySecurityPackageInfo</a> function.


#### - Reserved1

Reserved for future use.


#### - SetContextAttributes

Pointer to the   <a href="https://docs.microsoft.com/windows/desktop/api/sspi/nf-sspi-setcontextattributesa">SetContextAttributes</a> function.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sspi/nf-sspi-initsecurityinterfacea">InitSecurityInterface</a>
 

 


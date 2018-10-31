---
UID: NS:sspi._SECURITY_FUNCTION_TABLE_A
title: "_SECURITY_FUNCTION_TABLE_A"
author: windows-sdk-content
description: The SecurityFunctionTable structure is a dispatch table that contains pointers to the functions defined in SSPI.
old-location: security\securityfunctiontable.htm
tech.root: secauthn
ms.assetid: 6315e8d6-b40a-4dd6-b6a6-598a965f93dc
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "*PSecurityFunctionTableA, PSecurityFunctionTable, PSecurityFunctionTable structure pointer [Security], SECURITY_SUPPORT_PROVIDER_INTERFACE_VERSION, SECURITY_SUPPORT_PROVIDER_INTERFACE_VERSION structure [Security], SecurityFunctionTable, SecurityFunctionTable structure [Security], SecurityFunctionTableA, SecurityFunctionTableW, _SECURITY_FUNCTION_TABLE_A, _ssp_securityfunctiontable, security.securityfunctiontable, sspi/PSecurityFunctionTable, sspi/SECURITY_SUPPORT_PROVIDER_INTERFACE_VERSION, sspi/SecurityFunctionTable, sspi/SecurityFunctionTableA, sspi/SecurityFunctionTableW"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
---

# _SECURITY_FUNCTION_TABLE_A structure


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

Pointer to the <a href="https://msdn.microsoft.com/eaa15fed-4438-4e43-9be3-aa100ca453c7">AcceptSecurityContext (General)</a> function.


### -field CompleteAuthToken

Pointer to the <a href="https://msdn.microsoft.com/a404d0a3-d1ea-4708-87d7-2d216e9a5f5f">CompleteAuthToken</a> function.


### -field DeleteSecurityContext

Pointer to the <a href="https://msdn.microsoft.com/2a4dd697-ef90-4c37-ab74-0e5ab92794cd">DeleteSecurityContext</a> function.


### -field ApplyControlToken

Pointer to the <a href="https://msdn.microsoft.com/5ce13a05-874c-4e1a-9be8-aed98609791e">ApplyControlToken</a> function.


### -field QueryContextAttributesA

 


### -field ImpersonateSecurityContext

Pointer to the <a href="https://msdn.microsoft.com/167eaf3b-b794-4587-946d-fa596f1f9411">ImpersonateSecurityContext</a> function.


### -field RevertSecurityContext

Pointer to the <a href="https://msdn.microsoft.com/d4ed1fe9-2e0a-4648-a010-1eae49ba03ee">RevertSecurityContext</a> function.


### -field MakeSignature

Pointer to the <a href="https://msdn.microsoft.com/d17824b0-6121-48a3-b19b-d4fae3e1348e">MakeSignature</a> function.


### -field VerifySignature

Pointer to the <a href="https://msdn.microsoft.com/bebeef92-1d6e-4879-846f-12d706db0653">VerifySignature</a> function.


### -field FreeContextBuffer

Pointer to the <a href="https://msdn.microsoft.com/3c3d27bb-4f9a-4979-b679-1e10fa1ff221">FreeContextBuffer</a> function.


### -field QuerySecurityPackageInfoA

 


### -field Reserved3

Reserved for future use.


### -field Reserved4

Reserved for future use.


### -field ExportSecurityContext

Pointer to the <a href="https://msdn.microsoft.com/4ebc7f37-b948-4c78-973f-0a74e55c7ee2">ExportSecurityContext</a> function.


### -field ImportSecurityContextA

 


### -field AddCredentialsA

 


### -field Reserved8

Reserved for future use.


### -field QuerySecurityContextToken

Pointer to the  <a href="https://msdn.microsoft.com/5dc23608-9ce3-4fee-8161-2e409cef4063">QuerySecurityContextToken</a> function.


### -field EncryptMessage

Pointer to the  <a href="https://msdn.microsoft.com/2e09f262-9c3e-4db2-9285-017f5e1810c7">EncryptMessage (General)</a> function.


### -field DecryptMessage

Pointer to the   <a href="https://msdn.microsoft.com/ea271d0c-9167-41c5-8919-09611206fc71">DecryptMessage (General)</a> function.


### -field SetContextAttributesA

 


### -field SetCredentialsAttributesA

 


### -field ChangeAccountPasswordA

 


### -field Reserved9

 


### -field QueryContextAttributesExA

 


### -field QueryCredentialsAttributesExA

 




#### - AcquireCredentialsHandle

Pointer to the <a href="https://msdn.microsoft.com/acda4cf3-39a6-4bd2-91a0-db1f191b57b5">AcquireCredentialsHandle</a> function.


#### - AddCredentials

Pointer to the  <a href="https://msdn.microsoft.com/ea6ddd18-818e-43f5-9453-de2b3f994325">AddCredential</a> function.


#### - EnumerateSecurityPackages

Pointer to the <a href="https://msdn.microsoft.com/900790a6-111d-43f5-9316-e85aab03a3bc">EnumerateSecurityPackages</a> function.


#### - FreeCredentialsHandle

Pointer to the <a href="https://msdn.microsoft.com/e089618c-8233-475a-9725-39265c6427ab">FreeCredentialsHandle</a> function.


#### - ImportSecurityContext

Pointer to the <a href="https://msdn.microsoft.com/0f8e65d0-69cf-42ba-a903-1922d731e5ec">ImportSecurityContext</a> function.


#### - InitializeSecurityContext

Pointer to the  <a href="https://msdn.microsoft.com/21d965d4-3c03-4e29-a70d-4538c5c366b0">InitializeSecurityContext (General)</a> function.


#### - QueryContextAttributes

Pointer to the  <a href="https://msdn.microsoft.com/67bc087f-7519-4c8a-9b34-b3ecd306a334">QueryContextAttributes (General)</a> function.


#### - QueryCredentialsAttributes

Pointer to the  <a href="https://msdn.microsoft.com/a8ba6f73-8469-431b-b185-183b45b2c533">QueryCredentialsAttributes</a> function.


#### - QuerySecurityPackageInfo

Pointer to the   <a href="https://msdn.microsoft.com/130ef0fe-bb13-4a65-b476-cd25ed234da1">QuerySecurityPackageInfo</a> function.


#### - Reserved1

Reserved for future use.


#### - SetContextAttributes

Pointer to the   <a href="https://msdn.microsoft.com/e3246c3e-3e8c-49fe-99d8-dfff1a10ab83">SetContextAttributes</a> function.


## -see-also




<a href="https://msdn.microsoft.com/1026eeab-e2d6-45f2-9677-82d6cfbf4e12">InitSecurityInterface</a>
 

 


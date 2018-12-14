---
UID: NS:ntsecpkg._SECPKG_FUNCTION_TABLE
title: SECPKG_FUNCTION_TABLE
author: windows-sdk-content
description: The SECPKG_FUNCTION_TABLE structure contains pointers to the LSA functions that a security package must implement. The Local Security Authority (LSA) obtains this structure from an SSP/AP DLL when it calls the SpLsaModeInitialize function.
old-location: security\secpkg_function_table.htm
tech.root: secauthn
ms.assetid: 43ca0f9b-1393-48aa-9d9c-4dd19963a66d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PSECPKG_FUNCTION_TABLE, PSECPKG_FUNCTION_TABLE, PSECPKG_FUNCTION_TABLE structure pointer [Security], SECPKG_FUNCTION_TABLE, SECPKG_FUNCTION_TABLE structure [Security], _ssp_secpkg_function_table, ntsecpkg/PSECPKG_FUNCTION_TABLE, ntsecpkg/SECPKG_FUNCTION_TABLE, security.secpkg_function_table"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
 - HeaderDef
api_location:
 - Ntsecpkg.h
api_name:
 - SECPKG_FUNCTION_TABLE
product: Windows
targetos: Windows
req.typenames: SECPKG_FUNCTION_TABLE, *PSECPKG_FUNCTION_TABLE
req.redist: 
---

# SECPKG_FUNCTION_TABLE structure


## -description


The <b>SECPKG_FUNCTION_TABLE</b> structure contains pointers to the LSA functions that a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a> must implement. The <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">Local Security Authority</a> (LSA) obtains this structure from an SSP/AP DLL when it calls the 
<a href="https://msdn.microsoft.com/1ef3770b-197f-4d5b-9933-b7f6f63e5627">SpLsaModeInitialize</a> function.


## -struct-fields




### -field InitializePackage

Pointer to the <a href="https://msdn.microsoft.com/1fed5a5e-5dc1-4b59-aa28-bd1395a27742">LsaApInitializePackage</a> function.
					


### -field LogonUser

Pointer to the <a href="https://msdn.microsoft.com/a6d880a0-0aed-4bdb-89c9-4f667ecb510e">LogonUser</a> function.


### -field CallPackage

Pointer to the <a href="https://msdn.microsoft.com/770c41ab-df79-4371-9f1d-7bbce8193b5d">CallPackage</a> function.
					


### -field LogonTerminated

Pointer to the <a href="https://msdn.microsoft.com/17e8426a-5a25-48ca-8cef-91bbeda8490c">LsaApLogonTerminated</a> function.


### -field CallPackageUntrusted

Pointer to the <a href="https://msdn.microsoft.com/86320637-f224-494c-a48b-4c8b05a059df">LsaApCallPackageUntrusted</a>  function.


### -field CallPackagePassthrough

Pointer to the <a href="https://msdn.microsoft.com/622856ca-f49e-4995-bead-7b02501a84e5">CallPackagePassthrough</a> function.


### -field LogonUserEx

Pointer to the <a href="https://msdn.microsoft.com/4aba1cad-f234-4329-8599-7438cb9bee98">LogonUserEx</a> function.


### -field LogonUserEx2

Pointer to the <a href="https://msdn.microsoft.com/002ac773-bd46-49b5-b54c-6b8f5d5ef9f7">LsaApLogonUserEx2</a> function.


### -field Initialize

Pointer to the <a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a> function.


### -field Shutdown

Pointer to the <a href="https://msdn.microsoft.com/631f4664-adbb-4b12-9695-46eaced6ac44">SpShutdown</a> function.


### -field GetInfo

Pointer to the <a href="https://msdn.microsoft.com/e1e6f71f-6f54-424c-be49-7bc11cb19036">SpGetInfo</a> function.


### -field AcceptCredentials

Pointer to the <a href="https://msdn.microsoft.com/bb382937-e5d6-452b-b166-505d0c80412c">SpAcceptCredentials</a> function.


### -field AcquireCredentialsHandle

Pointer to the <a href="https://msdn.microsoft.com/acda4cf3-39a6-4bd2-91a0-db1f191b57b5">AcquireCredentialsHandle</a> function.


### -field QueryCredentialsAttributes

Pointer to the <a href="https://msdn.microsoft.com/a8ba6f73-8469-431b-b185-183b45b2c533">QueryCredentialsAttributes</a> function.


### -field FreeCredentialsHandle

Pointer to the <a href="https://msdn.microsoft.com/e089618c-8233-475a-9725-39265c6427ab">FreeCredentialsHandle</a> function.


### -field SaveCredentials

Pointer to the <a href="https://msdn.microsoft.com/15983acb-6fa3-4c53-9ede-a41db95c82f1">SpSaveCredentials</a> function.


### -field GetCredentials

Pointer to the <a href="https://msdn.microsoft.com/e9a2d112-6681-4400-b316-ffd7095e319a">GetCredentials</a> function.


### -field DeleteCredentials

Pointer to the <a href="https://msdn.microsoft.com/14f41fc2-1e28-4ae5-9f2e-00f2500b7819">SpDeleteCredentials</a> function.


### -field InitLsaModeContext

Pointer to the <a href="https://msdn.microsoft.com/e733d6fb-0ce6-4fd2-a8e2-54aa44602828">SpInitLsaModeContext</a> function.


### -field AcceptLsaModeContext

Pointer to the <a href="https://msdn.microsoft.com/bf443c15-0039-4ffa-a5ec-e8ef6a24dc80">SpAcceptLsaModeContext</a> function.


### -field DeleteContext

Pointer to the <a href="https://msdn.microsoft.com/70e64bd3-7fdf-464b-bc0a-a0384a3e1a59">SpDeleteContext</a> function.


### -field ApplyControlToken

Pointer to the <a href="https://msdn.microsoft.com/5ce13a05-874c-4e1a-9be8-aed98609791e">ApplyControlToken</a> function.


### -field GetUserInfo

Pointer to the <a href="https://msdn.microsoft.com/ee37fab0-5ee5-4cc5-9fcc-5c74cb0b2b26">SpGetUserInfo</a> function.


### -field GetExtendedInformation

Pointer to the <a href="https://msdn.microsoft.com/e3cb602a-2c98-4e9c-bfbc-f12f353ce3e3">SpGetExtendedInformation
</a> function.


### -field QueryContextAttributes

Pointer to the <a href="https://msdn.microsoft.com/67bc087f-7519-4c8a-9b34-b3ecd306a334">QueryContextAttributes (General)</a> function.


### -field AddCredentials

Pointer to the <a href="https://msdn.microsoft.com/27377afa-4e54-4c6b-8e84-a8810bc01139">SpAddCredentials</a> function.


### -field SetExtendedInformation

Pointer to the <a href="https://msdn.microsoft.com/a6176786-c19b-4ecf-8a7b-2430ff8b56f7">SpSetExtendedInformation</a> function.


### -field SetContextAttributes

Pointer to the <a href="https://msdn.microsoft.com/e3246c3e-3e8c-49fe-99d8-dfff1a10ab83">SetContextAttributes</a> function.


### -field SetCredentialsAttributes

Pointer to the <a href="https://msdn.microsoft.com/419fb4f0-3dd1-4473-aeb2-8024355e0c1c">SetCredentialsAttributes</a> function.


### -field ChangeAccountPassword

 


### -field QueryMetaData

Pointer to the <a href="https://msdn.microsoft.com/2409035b-34e9-4c43-9cb5-df46830fcc61">QueryMetaData</a> function.


### -field ExchangeMetaData

Pointer to the <a href="https://msdn.microsoft.com/35ef9276-1d61-44f3-912c-cf07dfcf7984">ExchangeMetaData</a> function.


### -field GetCredUIContext

Pointer to the <a href="https://msdn.microsoft.com/7cd20c78-8203-42a2-ad58-1a206fad5463">GetCredUIContext</a> function.


### -field UpdateCredentials

Pointer to the <a href="https://msdn.microsoft.com/56aba12e-a335-4d16-81b0-7ab521f872e7">UpdateCredentials</a> function.


### -field ValidateTargetInfo

Pointer to the <a href="https://msdn.microsoft.com/01d1b74a-14d9-40cd-bcca-a031f5fc9cbb">SpValidateTargetInfoFn</a> function.


### -field PostLogonUser

 


### -field GetRemoteCredGuardLogonBuffer

 


### -field GetRemoteCredGuardSupplementalCreds

 




#### - SpChangeAccountPasswordFn

Pointer to the <a href="https://msdn.microsoft.com/a1d1e315-d1a2-499a-b552-83180508271f">ChangeAccountPassword</a> function.


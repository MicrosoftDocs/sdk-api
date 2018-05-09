---
UID: NS:ntsecpkg._LSA_SECPKG_FUNCTION_TABLE
title: "_LSA_SECPKG_FUNCTION_TABLE"
author: windows-driver-content
description: Contains pointers to the LSA functions that a security package can call. The Local Security Authority (LSA) passes this structure to a security package when it calls the package's SpInitialize function.
old-location: security\lsa_secpkg_function_table.htm
old-project: SecAuthN
ms.assetid: 85f04072-8634-454a-9038-737d86c5597d
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: "*PLSA_SECPKG_FUNCTION_TABLE, LSA_SECPKG_FUNCTION_TABLE, LSA_SECPKG_FUNCTION_TABLE structure [Security], PLSA_SECPKG_FUNCTION_TABLE, PLSA_SECPKG_FUNCTION_TABLE structure pointer [Security], _LSA_SECPKG_FUNCTION_TABLE, _ssp_lsa_secpkg_function_table, ntsecpkg/LSA_SECPKG_FUNCTION_TABLE, ntsecpkg/PLSA_SECPKG_FUNCTION_TABLE, security.lsa_secpkg_function_table"
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
req.typenames: LSA_SECPKG_FUNCTION_TABLE, *PLSA_SECPKG_FUNCTION_TABLE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ntsecpkg.h
api_name:
-	LSA_SECPKG_FUNCTION_TABLE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# _LSA_SECPKG_FUNCTION_TABLE structure


## -description


The <b>LSA_SECPKG_FUNCTION_TABLE</b> structure contains pointers to the LSA functions that a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a> can call. The <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">Local Security Authority</a> (LSA) passes this structure to a security package when it calls the package's 
<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a> function.


## -struct-fields




### -field CreateLogonSession


					Pointer to the  <a href="https://msdn.microsoft.com/383c935c-a1f2-4d1b-bb02-e7e37f154771">CreateLogonSession</a> function.


### -field DeleteLogonSession

Pointer to the  <a href="https://msdn.microsoft.com/72b9451c-8a94-4e64-bd78-0afef210671c">DeleteLogonSession</a> function.
					


### -field AddCredential

Pointer to the  <a href="https://msdn.microsoft.com/ea6ddd18-818e-43f5-9453-de2b3f994325">AddCredential</a> function.
					


### -field GetCredentials

Pointer to the  <a href="https://msdn.microsoft.com/e9a2d112-6681-4400-b316-ffd7095e319a">GetCredentials</a> function.


### -field DeleteCredential

Pointer to the  <a href="https://msdn.microsoft.com/06bc02ec-5c07-41db-9f00-49773a597a09">DeleteCredential</a> function.
					


### -field AllocateLsaHeap

Pointer to the  <a href="https://msdn.microsoft.com/cb87f1b1-3e1e-4add-8e74-ca7b4f8599ba">AllocateLsaHeap</a> function.
					


### -field FreeLsaHeap

Pointer to the  <a href="https://msdn.microsoft.com/bd461a23-2501-48c5-8f2f-c6c98383157f">FreeLsaHeap</a> function.
					


### -field AllocateClientBuffer

Pointer to the  <a href="https://msdn.microsoft.com/2a7dfc11-a8ab-4677-ad5c-b2f4b5998efe">AllocateClientBuffer</a> function.
					


### -field FreeClientBuffer

Pointer to the  <a href="https://msdn.microsoft.com/c3a92039-7fb1-49e9-8e7a-0c902770543e">FreeClientBuffer</a> function.
					


### -field CopyToClientBuffer

Pointer to the  <a href="https://msdn.microsoft.com/53ea2c99-7934-447d-9ec5-e88ee925ca89">CopyToClientBuffer</a> function.
					


### -field CopyFromClientBuffer

Pointer to the  <a href="https://msdn.microsoft.com/d753694e-38f9-47d1-b860-252123ae6f16">CopyFromClientBuffer</a> function.
					


### -field ImpersonateClient

Pointer to the  <a href="https://msdn.microsoft.com/ec814a85-4f93-4a25-82f0-ce83caf37e5d">ImpersonateClient</a> function.
					


### -field UnloadPackage

Pointer to the  <a href="https://msdn.microsoft.com/93be186a-a87d-4bf5-b5dd-d5a551145e4b">UnloadPackage</a> function.
					


### -field DuplicateHandle

Pointer to the <a href="https://msdn.microsoft.com/1930a33c-2921-4ac1-994a-ee4686d6a66b">DuplicateHandle</a>  function.
					


### -field SaveSupplementalCredentials

Pointer to the <b>SaveSupplementalCredentials</b>  function.
					


### -field CreateThread

Pointer to the <a href="https://msdn.microsoft.com/dc02abb9-ab05-4a7f-a125-15530619633b">CreateThread</a>  function.
					


### -field GetClientInfo

Pointer to the <a href="https://msdn.microsoft.com/3669f2e2-da70-4195-bdd0-f8415d97ae99">GetClientInfo</a>  function.
					


### -field RegisterNotification

Pointer to the <a href="https://msdn.microsoft.com/689a1956-5eab-4eec-93ef-5ddcef6546ee">RegisterNotification</a>  function.
					


### -field CancelNotification

Pointer to the  <a href="https://msdn.microsoft.com/b7333318-ee17-4cc2-9382-2d4871ddee78">CancelNotification</a> function.
					


### -field MapBuffer

Pointer to the <a href="https://msdn.microsoft.com/3189da1b-5f2f-4569-8f60-6f3b287460f1">MapBuffer</a>  function.
					


### -field CreateToken

Pointer to the  <a href="https://msdn.microsoft.com/2355cf1d-9f95-40be-aed4-8c2796137960">CreateToken</a> function.
					


### -field AuditLogon

Pointer to the   <a href="https://msdn.microsoft.com/1b0316ae-0c09-4a7e-8443-e59b4db9e825">AuditLogon</a> function.
					


### -field CallPackage

Pointer to the <a href="https://msdn.microsoft.com/770c41ab-df79-4371-9f1d-7bbce8193b5d">CallPackage</a>  function.
					


### -field FreeReturnBuffer

Pointer to the  <a href="https://msdn.microsoft.com/44b7e6f2-eb7e-47ec-8252-689eb1e5aa77">FreeReturnBuffer</a> function.
					


### -field GetCallInfo

Pointer to the  <a href="https://msdn.microsoft.com/3e59ee6a-f7ba-4886-98f7-74ffbfaadea7">GetCallInfo</a> function.
					


### -field CallPackageEx

Pointer to the <a href="https://msdn.microsoft.com/b26eb42d-9692-4df7-bbde-f7bce0924221">CallPackageEx</a>  function.
					


### -field CreateSharedMemory

Pointer to the <a href="https://msdn.microsoft.com/22abafd7-1648-4bea-a0a8-0cb58333fbea">CreateSharedMemory</a>  function.
					


### -field AllocateSharedMemory

Pointer to the   <a href="https://msdn.microsoft.com/77fdedaf-8931-4412-ab35-bd3de8e78b9a">AllocateSharedMemory</a> function.
					


### -field FreeSharedMemory

Pointer to the <a href="https://msdn.microsoft.com/def16ef0-4ae7-43c5-99c8-493bdf0c6a97">FreeSharedMemory</a>  function.
					


### -field DeleteSharedMemory

Pointer to the <a href="https://msdn.microsoft.com/8059ff30-6301-4cf6-9620-2ba765303bb4">DeleteSharedMemory</a>  function.
					


### -field OpenSamUser

Pointer to the <a href="https://msdn.microsoft.com/1d9bfbe5-8dd2-4b0f-a19a-361eef8901a4">OpenSamUser</a>  function.
					


### -field GetUserCredentials

Pointer to the  <b>GetUserCredentials</b> function.
					


### -field GetUserAuthData

Pointer to the  <a href="https://msdn.microsoft.com/2436eaee-1f32-4e32-9a98-74968ad9b58e">GetUserAuthData</a> function.
					


### -field CloseSamUser

Pointer to the  <a href="https://msdn.microsoft.com/1e56e38e-ba8f-4781-80f1-e60bd33250e4">CloseSamUser</a> function.
					


### -field ConvertAuthDataToToken

Pointer to the  <a href="https://msdn.microsoft.com/99dfd3b3-40e0-44b2-8752-39b7b394ac0e">ConvertAuthDataToToken</a> function.
					


### -field ClientCallback

Pointer to the  <a href="https://msdn.microsoft.com/d818a7b5-15c8-4d25-a8de-050926f34a9d">ClientCallback</a> function.
					


### -field UpdateCredentials

Pointer to the  <a href="https://msdn.microsoft.com/952ed682-775a-4370-8a89-15ca35553667">UpdateCredentials</a> function.
					


### -field GetAuthDataForUser

Pointer to the  <a href="https://msdn.microsoft.com/1cc02c6b-2628-441d-97ae-ed83a4f6bfd0">GetAuthDataForUser</a> function.
					


### -field CrackSingleName

Pointer to the  <a href="https://msdn.microsoft.com/de42ca97-4ce2-4bfb-abd1-7409cc5c09a8">CrackSingleName</a> function.
					


### -field AuditAccountLogon

Pointer to the  <a href="https://msdn.microsoft.com/dcf2d16b-8352-4d40-9723-c8cf8465431c">AuditAccountLogon</a> function.
					


### -field CallPackagePassthrough

Pointer to the <a href="https://msdn.microsoft.com/622856ca-f49e-4995-bead-7b02501a84e5">CallPackagePassthrough</a> function.
					


### -field CrediRead

Pointer to the <a href="https://msdn.microsoft.com/b6abfde9-74ac-4af0-b8ab-4f6be937f17f">CrediRead</a> function.


### -field CrediReadDomainCredentials

Pointer to the <a href="https://msdn.microsoft.com/fa5c92be-c74b-4143-8526-b60c25461b8c">CrediReadDomainCredentials</a> function.


### -field CrediFreeCredentials

Pointer to the <a href="https://msdn.microsoft.com/9da22201-884d-4822-a769-c2ce0d36ec73">CrediFreeCredentials</a> function.


### -field DummyFunction1

 


### -field DummyFunction2

 


### -field DummyFunction3

 


### -field LsaProtectMemory

Pointer to the <a href="https://msdn.microsoft.com/c851fe8b-be22-4966-ab99-f177989cf382">LsaProtectMemory</a> function.


### -field LsaUnprotectMemory

Pointer to the <a href="https://msdn.microsoft.com/3a9306a1-8325-4ccf-a611-4740b16cf343">LsaUnprotectMemory</a> function.


### -field OpenTokenByLogonId

Pointer to the <a href="https://msdn.microsoft.com/3cd3e4fe-7548-44f9-ab04-01b30bdf3bd9">OpenTokenByLogonId</a> function.


### -field ExpandAuthDataForDomain

Pointer to the <a href="https://msdn.microsoft.com/965d8575-a05b-45d8-8718-4004f1d22ca5">ExpandAuthDataForDomain</a> function.


### -field AllocatePrivateHeap

Pointer to the <a href="https://msdn.microsoft.com/956e7aaf-e8b3-4db5-945a-b579f946b769">AllocatePrivateHeap</a> function.


### -field FreePrivateHeap

Pointer to the <a href="https://msdn.microsoft.com/f1ca1450-c59c-4c0f-b68b-373f1a7c70da">FreePrivateHeap</a> function.


### -field CreateTokenEx

Pointer to the <a href="https://msdn.microsoft.com/1f12d8a4-6cbd-43e3-98a7-eaf3d30a053e">CreateTokenEx</a> function.


### -field CrediWrite

Pointer to the <a href="https://msdn.microsoft.com/19c7fe4d-9c7b-4547-baab-443483deb013">CrediWrite</a> function.


### -field CrediUnmarshalandDecodeString

Pointer to the <a href="https://msdn.microsoft.com/15423c8d-ea3b-4981-b059-5828555a9e89">CrediUnmarshalandDecodeString</a> function.

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


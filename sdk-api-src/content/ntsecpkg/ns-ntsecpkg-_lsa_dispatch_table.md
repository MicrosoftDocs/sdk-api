---
UID: NS:ntsecpkg._LSA_DISPATCH_TABLE
title: "_LSA_DISPATCH_TABLE"
author: windows-sdk-content
description: Contains pointers to the Local Security Authority (LSA) functions that Windows authentication packages can call.
old-location: security\lsa_dispatch_table.htm
tech.root: secauthn
ms.assetid: 2e144ce0-e8c9-457a-8b12-7d21dda6adf3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PLSA_DISPATCH_TABLE, LSA_DISPATCH_TABLE, LSA_DISPATCH_TABLE structure [Security], PLSA_DISPATCH_TABLE, PLSA_DISPATCH_TABLE structure pointer [Security], _LSA_DISPATCH_TABLE, _lsa_lsa_dispatch_table, ntsecpkg/LSA_DISPATCH_TABLE, ntsecpkg/PLSA_DISPATCH_TABLE, security.lsa_dispatch_table"
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
 - LSA_DISPATCH_TABLE
product: Windows
targetos: Windows
req.typenames: LSA_DISPATCH_TABLE, *PLSA_DISPATCH_TABLE
req.redist: 
---

# _LSA_DISPATCH_TABLE structure


## -description


The <b>LSA_DISPATCH_TABLE</b> structure contains pointers to the <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">Local Security Authority</a> (LSA) functions that Windows <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">authentication packages</a> can call.

The LSA passes this structure to an authentication package when it calls the  
<a href="https://msdn.microsoft.com/1fed5a5e-5dc1-4b59-aa28-bd1395a27742">LsaApInitializePackage</a> function of the package.


## -struct-fields




### -field CreateLogonSession

Pointer to the <a href="https://msdn.microsoft.com/383c935c-a1f2-4d1b-bb02-e7e37f154771">CreateLogonSession</a> function.


### -field DeleteLogonSession

Pointer to the <a href="https://msdn.microsoft.com/72b9451c-8a94-4e64-bd78-0afef210671c">DeleteLogonSession</a> function.


### -field AddCredential

Pointer to the 
					<a href="https://msdn.microsoft.com/ea6ddd18-818e-43f5-9453-de2b3f994325">AddCredential</a> function.


### -field GetCredentials

Pointer to the <a href="https://msdn.microsoft.com/e9a2d112-6681-4400-b316-ffd7095e319a">GetCredentials</a> function.


### -field DeleteCredential

Pointer to the
					<a href="https://msdn.microsoft.com/06bc02ec-5c07-41db-9f00-49773a597a09">DeleteCredential</a> function.


### -field AllocateLsaHeap

Pointer to the
					<a href="https://msdn.microsoft.com/cb87f1b1-3e1e-4add-8e74-ca7b4f8599ba">AllocateLsaHeap</a> function.


### -field FreeLsaHeap

Pointer to the
					<a href="https://msdn.microsoft.com/bd461a23-2501-48c5-8f2f-c6c98383157f">FreeLsaHeap</a> function.


### -field AllocateClientBuffer

Pointer to the
					<a href="https://msdn.microsoft.com/2a7dfc11-a8ab-4677-ad5c-b2f4b5998efe">AllocateClientBuffer</a> function.


### -field FreeClientBuffer

Pointer to the
					<a href="https://msdn.microsoft.com/c3a92039-7fb1-49e9-8e7a-0c902770543e">FreeClientBuffer</a> function.


### -field CopyToClientBuffer

Pointer to the
					<a href="https://msdn.microsoft.com/53ea2c99-7934-447d-9ec5-e88ee925ca89">CopyToClientBuffer</a>  function.


### -field CopyFromClientBuffer

Pointer to the <a href="https://msdn.microsoft.com/d753694e-38f9-47d1-b860-252123ae6f16">CopyFromClientBuffer</a> function.


---
UID: NS:wintrust._CRYPT_PROVIDER_FUNCTIONS
title: "_CRYPT_PROVIDER_FUNCTIONS"
author: windows-sdk-content
description: Defines the functions used by a cryptographic service provider (CSP) for WinTrust operations.
old-location: security\crypt_provider_functions.htm
old-project: SecCrypto
ms.assetid: 2c00f8ec-e262-4df8-8984-a2702a4162bf
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: "*PCRYPT_PROVIDER_FUNCTIONS, CRYPT_PROVIDER_FUNCTIONS, CRYPT_PROVIDER_FUNCTIONS structure [Security], PCRYPT_PROVIDER_FUNCTIONS, PCRYPT_PROVIDER_FUNCTIONS structure pointer [Security], _CRYPT_PROVIDER_FUNCTIONS, security.crypt_provider_functions, wintrust/CRYPT_PROVIDER_FUNCTIONS, wintrust/PCRYPT_PROVIDER_FUNCTIONS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wintrust.h
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
tech.root: 
req.typenames: CRYPT_PROVIDER_FUNCTIONS, *PCRYPT_PROVIDER_FUNCTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wintrust.h
api_name:
-	CRYPT_PROVIDER_FUNCTIONS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _CRYPT_PROVIDER_FUNCTIONS structure


## -description


<p class="CCE_Message">[The  <b>CRYPT_PROVIDER_FUNCTIONS</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CRYPT_PROVIDER_FUNCTIONS</b> structure defines the functions  used by 	a cryptographic service provider (CSP) for WinTrust operations.


## -struct-fields




### -field cbStruct

The size, in bytes, of this structure.


### -field pfnAlloc

A pointer to the memory allocation function.


### -field pfnFree

A pointer to the memory deallocation function.


### -field pfnAddStore2Chain

A pointer to the function that adds a store to the chain.


### -field pfnAddSgnr2Chain

A pointer to the function that adds a signer structure to a message structure in a chain.


### -field pfnAddCert2Chain

A pointer to the function that adds a certificate structure to a signer structure in a chain.


### -field pfnAddPrivData2Chain

A pointer to the function that adds private data to a structure.


### -field pfnInitialize

A pointer to the function that initializes policy data.


### -field pfnObjectTrust

A pointer to the function that builds information for the signer data.


### -field pfnSignatureTrust

A pointer to the function that builds information for the signing certificate.


### -field pfnCertificateTrust

A pointer to the function that builds the chain.


### -field pfnFinalPolicy

A pointer to the function that makes the final call to the policy.


### -field pfnCertCheckPolicy

A pointer to the function that checks each certificate while building a chain.


### -field pfnTestFinalPolicy

A pointer to the function that allows structures to be dumped to a file.


### -field psUIpfns

A pointer to a <a href="https://msdn.microsoft.com/7cdc32ea-b28a-400f-ad8a-984f86bb95fd">CRYPT_PROVUI_FUNCS</a> structure.


### -field pfnCleanupPolicy

A pointer to the function that cleans up private data.


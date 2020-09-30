---
UID: NS:wintrust._CRYPT_PROVIDER_FUNCTIONS
title: CRYPT_PROVIDER_FUNCTIONS (wintrust.h)
description: Defines the functions used by a cryptographic service provider (CSP) for WinTrust operations.
helpviewer_keywords: ["*PCRYPT_PROVIDER_FUNCTIONS","CRYPT_PROVIDER_FUNCTIONS","CRYPT_PROVIDER_FUNCTIONS structure [Security]","PCRYPT_PROVIDER_FUNCTIONS","PCRYPT_PROVIDER_FUNCTIONS structure pointer [Security]","security.crypt_provider_functions","wintrust/CRYPT_PROVIDER_FUNCTIONS","wintrust/PCRYPT_PROVIDER_FUNCTIONS"]
old-location: security\crypt_provider_functions.htm
tech.root: security
ms.assetid: 2c00f8ec-e262-4df8-8984-a2702a4162bf
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_PROVIDER_FUNCTIONS, CRYPT_PROVIDER_FUNCTIONS, CRYPT_PROVIDER_FUNCTIONS structure [Security], PCRYPT_PROVIDER_FUNCTIONS, PCRYPT_PROVIDER_FUNCTIONS structure pointer [Security], security.crypt_provider_functions, wintrust/CRYPT_PROVIDER_FUNCTIONS, wintrust/PCRYPT_PROVIDER_FUNCTIONS'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CRYPT_PROVIDER_FUNCTIONS, *PCRYPT_PROVIDER_FUNCTIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_PROVIDER_FUNCTIONS
 - wintrust/_CRYPT_PROVIDER_FUNCTIONS
 - PCRYPT_PROVIDER_FUNCTIONS
 - wintrust/PCRYPT_PROVIDER_FUNCTIONS
 - CRYPT_PROVIDER_FUNCTIONS
 - wintrust/CRYPT_PROVIDER_FUNCTIONS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wintrust.h
api_name:
 - CRYPT_PROVIDER_FUNCTIONS
---

# CRYPT_PROVIDER_FUNCTIONS structure


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

A pointer to a <a href="/windows/desktop/api/wintrust/ns-wintrust-crypt_provui_funcs">CRYPT_PROVUI_FUNCS</a> structure.

### -field pfnCleanupPolicy

A pointer to the function that cleans up private data.
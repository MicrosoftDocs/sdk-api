---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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


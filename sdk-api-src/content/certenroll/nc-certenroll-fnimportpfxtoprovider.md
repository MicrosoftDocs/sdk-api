---
UID: NC:certenroll.FNIMPORTPFXTOPROVIDER
title: ImportPFXToProvider
author: windows-sdk-content
description: Imports a PFX certificate.
old-location: security\fnimportpfxtoprovider.htm
tech.root: SecCrypto
ms.assetid: D5F4A318-4572-4563-85B0-7F3532833DE4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "ImportPFXToProvider, (FNIMPORTPFXTOPROVIDER), (FNIMPORTPFXTOPROVIDER) callback function [Security], FNIMPORTPFXTOPROVIDER callback, certenroll/(FNIMPORTPFXTOPROVIDER), fnimportpfxtoprovider, security.fnimportpfxtoprovider, wincrypt/(FNIMPORTPFXTOPROVIDER)"
ms.topic: callback
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - certenroll.h
 - wincrypt.h
api_name:
 - (FNIMPORTPFXTOPROVIDER)
 - ImportPFXToProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ImportPFXToProvider callback function


## -description


Imports a PFX certificate.


## -parameters




### -param hWndParent [in]

Handle toa Parent Window.


### -param *pbPFX [in]

Pointer to a buffer that contains the PFX file.


### -param cbPFX [in]

Size of pbPFX in bytes.


### -param ImportFlags [in]

One or more <a href="https://msdn.microsoft.com/en-us/library/Mt832769(v=VS.85).aspx">ImportPFXFlag</a> values.


### -param pwszPassword [in, optional]

Pointer to a constant null-terminated string of 16-bit Unicode characters that is the Password for the PFX file.


### -param pwszProviderName [in, optional]

Pointer to a constant null-terminated string of 16-bit Unicode characters that is the name of the crypto provider.


### -param pwszReaderName [in, optional]

Pointer to a constant null-terminated string of 16-bit Unicode characters that is the name of the smart card reader (can be nullptr).


### -param pwszContainerNamePrefix [in, optional]

Pointer to a constant null-terminated string of 16-bit Unicode characters that is the name of the container (can be nullptr).


### -param pwszPin [in, optional]

Pointer to a constant null-terminated string of 16-bit Unicode characters that is the PIN of the smart card (can be nullptr).


### -param pwszFriendlyName [in, optional]

Pointer to a constant null-terminated string of 16-bit Unicode characters that is the friendly name of the certificate (can be nullptr).


### -param *pcCertOut [out, optional]

Pointer to DWORD that receives  the number of certificates successfully imported (can be nullptr).


#### - **prgpCertOut [out, optional]

Pointer to a pointer that receives a <a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> structure (can be nullptr).


#### - prgpCertOut [out, optional]

Pointer to a pointer that receives a <a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> structure (can be nullptr).


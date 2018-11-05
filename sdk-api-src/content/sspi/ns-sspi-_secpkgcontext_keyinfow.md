---
UID: NS:sspi._SecPkgContext_KeyInfoW
title: "_SecPkgContext_KeyInfoW"
author: windows-sdk-content
description: The SecPkgContext_KeyInfo structure contains information about the session keys used in a security context.
old-location: security\secpkgcontext_keyinfo.htm
tech.root: secauthn
ms.assetid: ec146329-6789-460c-ae62-629a1765a4c1
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*PSecPkgContext_KeyInfoW, PSecPkgContext_KeyInfo, PSecPkgContext_KeyInfo structure pointer [Security], SecPkgContext_KeyInfo, SecPkgContext_KeyInfo structure [Security], SecPkgContext_KeyInfoA, SecPkgContext_KeyInfoW, _SecPkgContext_KeyInfoW, _ssp_secpkgcontext_keyinfo, security.secpkgcontext_keyinfo, sspi/PSecPkgContext_KeyInfo, sspi/SecPkgContext_KeyInfo, sspi/SecPkgContext_KeyInfoA, sspi/SecPkgContext_KeyInfoW"
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
req.unicode-ansi: SecPkgContext_KeyInfoW (Unicode) and SecPkgContext_KeyInfoA (ANSI)
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
 - SecPkgContext_KeyInfo
 - SecPkgContext_KeyInfoA
 - SecPkgContext_KeyInfoW
product: Windows
targetos: Windows
req.typenames: SecPkgContext_KeyInfoW, *PSecPkgContext_KeyInfoW
req.redist: 
---

# _SecPkgContext_KeyInfoW structure


## -description


The <b>SecPkgContext_KeyInfo</b> structure contains information about the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">session keys</a> used in a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a>. The 
<a href="https://msdn.microsoft.com/67bc087f-7519-4c8a-9b34-b3ecd306a334">QueryContextAttributes (General)</a> function uses this structure.

Applications using the Schannel <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security support provider</a> (SSP) should not use the <b>SecPkgContext_KeyInfo</b> structure. Instead, use the <a href="https://msdn.microsoft.com/5380c03b-d2c5-4a0d-96a1-c39305b9c9ac">SecPkgContext_ConnectionInfo</a> structure.


## -struct-fields




### -field sSignatureAlgorithmName

Pointer to a null-terminated string that contains the name, if available, of the algorithm used for generating signatures, for example "MD5" or "SHA-2".


### -field sEncryptAlgorithmName

Pointer to a null-terminated string that contains the name, if available, of the algorithm used for encrypting messages. Reserved for future use.


### -field KeySize

Specifies the effective key length, in bits, for the session key. This is typically 40, 56, or 128 bits.


### -field SignatureAlgorithm

Specifies the algorithm identifier (<a href="https://msdn.microsoft.com/557436b4-f7f1-4708-acc7-c6b47e6322ad">ALG_ID</a>) used for generating signatures, if available.


### -field EncryptAlgorithm

Specifies the algorithm identifier (<a href="https://msdn.microsoft.com/557436b4-f7f1-4708-acc7-c6b47e6322ad">ALG_ID</a>) used for encrypting messages. Reserved for future use.


## -see-also




<a href="https://msdn.microsoft.com/67bc087f-7519-4c8a-9b34-b3ecd306a334">QueryContextAttributes (General)</a>
 

 


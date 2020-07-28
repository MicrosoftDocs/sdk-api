---
UID: NS:sspi._SecPkgCredentials_SSIProviderW
title: SecPkgCredentials_SSIProviderW (sspi.h)
description: The SecPkgCredentials_SSIProvider structure holds the SSI provider information associated with a context. The QueryCredentialsAttributes function uses this structure.
helpviewer_keywords: ["*PSecPkgCredentials_SSIProviderW","PSecPkgCredentials_SSIProvider","PSecPkgCredentials_SSIProvider structure pointer [Security]","SecPkgCredentials_SSIProvider","SecPkgCredentials_SSIProvider structure [Security]","SecPkgCredentials_SSIProviderA","SecPkgCredentials_SSIProviderW","security.secpkgcredentials_ssiprovider","sspi/PSecPkgCredentials_SSIProvider","sspi/SecPkgCredentials_SSIProvider","sspi/SecPkgCredentials_SSIProviderA","sspi/SecPkgCredentials_SSIProviderW"]
old-location: security\secpkgcredentials_ssiprovider.htm
tech.root: security
ms.assetid: 0C6D6217-3A97-40B5-A7FB-B9D49C5FBC7C
ms.date: 12/05/2018
ms.keywords: '*PSecPkgCredentials_SSIProviderW, PSecPkgCredentials_SSIProvider, PSecPkgCredentials_SSIProvider structure pointer [Security], SecPkgCredentials_SSIProvider, SecPkgCredentials_SSIProvider structure [Security], SecPkgCredentials_SSIProviderA, SecPkgCredentials_SSIProviderW, security.secpkgcredentials_ssiprovider, sspi/PSecPkgCredentials_SSIProvider, sspi/SecPkgCredentials_SSIProvider, sspi/SecPkgCredentials_SSIProviderA, sspi/SecPkgCredentials_SSIProviderW'
f1_keywords:
- sspi/SecPkgCredentials_SSIProvider
dev_langs:
- c++
req.header: sspi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SecPkgCredentials_SSIProviderW (Unicode) and SecPkgCredentials_SSIProviderA (ANSI)
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
- SecPkgCredentials_SSIProvider
- SecPkgCredentials_SSIProviderA
- SecPkgCredentials_SSIProviderW
targetos: Windows
req.typenames: SecPkgCredentials_SSIProviderW, *PSecPkgCredentials_SSIProviderW
req.redist: 
ms.custom: 19H1
---

# SecPkgCredentials_SSIProviderW structure


## -description


The <b>SecPkgCredentials_SSIProvider</b> structure holds the SSI provider information associated with a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">context</a>. The 
<a href="https://docs.microsoft.com/windows/desktop/api/sspi/nf-sspi-querycredentialsattributesa">QueryCredentialsAttributes</a> function uses this structure.


## -struct-fields




### -field sProviderName

Pointer to a null-terminated string that contains the name of the provider represented by the credential.


### -field ProviderInfoLength

Length of the provider information.


### -field ProviderInfo

The provider information.

## -remarks

> [!NOTE]
> The sspi.h header defines SecPkgCredentials_SSIProvider as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).


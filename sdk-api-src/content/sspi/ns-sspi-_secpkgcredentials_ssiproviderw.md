---
UID: NS:sspi._SecPkgCredentials_SSIProviderW
title: "_SecPkgCredentials_SSIProviderW"
author: windows-sdk-content
description: The SecPkgCredentials_SSIProvider structure holds the SSI provider information associated with a context. The QueryCredentialsAttributes function uses this structure.
old-location: security\secpkgcredentials_ssiprovider.htm
old-project: secauthn
ms.assetid: 0C6D6217-3A97-40B5-A7FB-B9D49C5FBC7C
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PSecPkgCredentials_SSIProviderW, PSecPkgCredentials_SSIProvider, PSecPkgCredentials_SSIProvider structure pointer [Security], SecPkgCredentials_SSIProvider, SecPkgCredentials_SSIProvider structure [Security], SecPkgCredentials_SSIProviderA, SecPkgCredentials_SSIProviderW, _SecPkgCredentials_SSIProviderW, security.secpkgcredentials_ssiprovider, sspi/PSecPkgCredentials_SSIProvider, sspi/SecPkgCredentials_SSIProvider, sspi/SecPkgCredentials_SSIProviderA, sspi/SecPkgCredentials_SSIProviderW"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: sspi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: SecPkgCredentials_SSIProviderW, *PSecPkgCredentials_SSIProviderW
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
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# _SecPkgCredentials_SSIProviderW structure


## -description


The <b>SecPkgCredentials_SSIProvider</b> structure holds the SSI provider information associated with a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">context</a>. The 
<a href="https://msdn.microsoft.com/a8ba6f73-8469-431b-b185-183b45b2c533">QueryCredentialsAttributes</a> function uses this structure.


## -struct-fields




### -field sProviderName

Pointer to a null-terminated string that contains the name of the provider represented by the credential.


### -field ProviderInfoLength

Length of the provider information.


### -field ProviderInfo

The provider information.


---
UID: NC:wincrypt.PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE
title: PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE
author: windows-driver-content
description: Initializes the provider.
old-location: security\pfn_crypt_object_locator_provider_initialize.htm
old-project: SecCrypto
ms.assetid: DBDE5B98-AC31-4CA0-A7C6-1FCD8FAC51FC
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE, PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE function pointer [Security], security.pfn_crypt_object_locator_provider_initialize, wincrypt/PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: USERNAME_TARGET_CREDENTIAL_INFO, *PUSERNAME_TARGET_CREDENTIAL_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Wincrypt.h
api_name:
-	PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE callback


## -description


The  <b>PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE</b> function initializes the provider. You must implement this function as part of your custom provider.


## -parameters




### -param pfnFlush [in]

Pointer to the <a href="https://msdn.microsoft.com/F6EE5424-A3ED-4E90-897B-56C605EB985C">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FLUSH</a> function implementation.


### -param pContext [in]

Pointer to a provider defined object that contains information about the provider and the objects.


### -param *pdwExpectedObjectCount [out]

Specifies the number of unique objects that the provider expects to locate. This value tells the caller how much memory to allocate for storing objects. Set this value to zero (0) to specify the default value of 10,000 objects.


### -param *ppFuncTable [out]

A <a href="https://msdn.microsoft.com/4B319A83-C230-4BFE-AF21-1395ED2D234B">CRYPT_OBJECT_LOCATOR_PROVIDER_TABLE</a> structure that contains pointers to the functions implemented by the provider. No pointers in the table can be <b>NULL</b>. The caller does not free this structure. It is expected that the provider will return a table that is not allocated on the heap.


#### - **ppPluginContext [out]

Pointer to an optional buffer defined by this provider. The buffer is not modified by the caller. Your provider can use the data to help it determine what actions to perform or to maintain additional information. This value may be set to <b>NULL</b>.


#### - ppPluginContext [out]

Pointer to an optional buffer defined by this provider. The buffer is not modified by the caller. Your provider can use the data to help it determine what actions to perform or to maintain additional information. This value may be set to <b>NULL</b>.


## -returns



If the function succeeds, return nonzero (<b>TRUE</b>).

If the function fails, return zero (<b>FALSE</b>) and specify an appropriate error in the <a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a> function. Most errors are passed through Schannel unaltered but this behavior is not guaranteed. Some errors may be mapped to other errors.




## -remarks



 The <b>PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE</b> function is currently called by only the Secure Channel (Schannel) security service provider (SSP). The Cryptography API (CAPI) will internally call your custom provider if, beginning with Windows 8, you specify the name of the security principal in the <i>pszPrincipal</i> parameter of the <a href="https://msdn.microsoft.com/0f006670-a1e5-47ed-baf5-ed55bd42b468">AcquireCredentialsHandle</a> function.

When you implement this function, remember to fill the  <a href="https://msdn.microsoft.com/4B319A83-C230-4BFE-AF21-1395ED2D234B">CRYPT_OBJECT_LOCATOR_PROVIDER_TABLE</a> function table with pointers to the following functions implemented by your provider:

<ul>
<li>
<a href="https://msdn.microsoft.com/2073915D-F23B-41BD-8376-4493FE9D62C6">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_GET</a>
</li>
<li>
<a href="https://msdn.microsoft.com/DDF1243D-A6C8-426A-A800-018E7FF7E182">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_RELEASE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/C05D5024-9A67-4EA8-9F61-D31AF3AE8545">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_PASSWORD</a>
</li>
<li>
<a href="https://msdn.microsoft.com/4C27BF58-79AB-4AD3-8D43-EEE7F73071D2">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/C2ED3B51-8B98-412C-A571-D107F2BEC5F1">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_IDENTIFIER</a>
</li>
</ul>
You must call <a href="https://msdn.microsoft.com/9633cce4-538e-490e-8a5a-6b28f161a09d">CryptRegisterDefaultOIDFunction</a> to register the provider in the Windows registry.




## -see-also




<a href="https://msdn.microsoft.com/4B319A83-C230-4BFE-AF21-1395ED2D234B">CRYPT_OBJECT_LOCATOR_PROVIDER_TABLE</a>



<a href="https://msdn.microsoft.com/F6EE5424-A3ED-4E90-897B-56C605EB985C">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FLUSH</a>
 

 


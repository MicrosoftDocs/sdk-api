---
UID: NC:wincrypt.PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_PASSWORD
title: PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_PASSWORD
author: windows-sdk-content
description: Releases the password used to encrypt a personal information exchange (PFX) byte array.
old-location: security\pfn_crypt_object_locator_provider_free_password.htm
tech.root: seccrypto
ms.assetid: C05D5024-9A67-4EA8-9F61-D31AF3AE8545
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_PASSWORD, PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_PASSWORD callback, PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_PASSWORD callback function [Security], security.pfn_crypt_object_locator_provider_free_password, wincrypt/PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_PASSWORD
ms.prod: windows
ms.technology: windows-sdk
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wincrypt.h
api_name:
 - PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_PASSWORD
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_PASSWORD callback function


## -description


The <b>PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_PASSWORD</b> callback function releases the password used to encrypt a personal information exchange (PFX) byte array.


## -parameters




### -param pPluginContext [in, optional]

Pointer to an optional buffer defined by this provider and returned by the <a href="https://msdn.microsoft.com/DBDE5B98-AC31-4CA0-A7C6-1FCD8FAC51FC">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE</a> function. The buffer is not modified by the caller. Your provider can use the data to help it determine what actions to perform or to maintain additional information. 


### -param pwszPassword [in]

Null-terminated Unicode string that contains the password.


## -returns



Do not return a value from this function. 




## -remarks



The <b>PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_PASSWORD</b> function is currently called by only the Secure Channel (Schannel) security package. Schannel calls <a href="https://msdn.microsoft.com/2073915D-F23B-41BD-8376-4493FE9D62C6">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_GET</a> to retrieve a PFX byte array and then calls <b>PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_PASSWORD</b> after the byte array has been processed but before calling the <a href="https://msdn.microsoft.com/C2ED3B51-8B98-412C-A571-D107F2BEC5F1">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_IDENTIFIER</a> function.




## -see-also




<a href="https://msdn.microsoft.com/4B319A83-C230-4BFE-AF21-1395ED2D234B">CRYPT_OBJECT_LOCATOR_PROVIDER_TABLE</a>



<a href="https://msdn.microsoft.com/2073915D-F23B-41BD-8376-4493FE9D62C6">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_GET</a>



<a href="https://msdn.microsoft.com/DBDE5B98-AC31-4CA0-A7C6-1FCD8FAC51FC">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE</a>
 

 


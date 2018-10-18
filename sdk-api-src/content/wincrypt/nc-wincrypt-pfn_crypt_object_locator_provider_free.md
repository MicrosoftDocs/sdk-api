---
UID: NC:wincrypt.PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE
title: PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE
author: windows-sdk-content
description: Releases the object returned by the provider.
old-location: security\pfn_crypt_object_locator_provider_free.htm
tech.root: seccrypto
ms.assetid: 4C27BF58-79AB-4AD3-8D43-EEE7F73071D2
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE, PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE callback, PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE callback function [Security], security.pfn_crypt_object_locator_provider_free, wincrypt/PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE
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
 - PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE callback function


## -description


The <b>PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE</b> callback function releases the object returned by the provider.


## -parameters




### -param pPluginContext [in, optional]

Pointer to an optional buffer defined by this provider and returned by the <a href="https://msdn.microsoft.com/DBDE5B98-AC31-4CA0-A7C6-1FCD8FAC51FC">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE</a> function. The buffer is not modified by the caller. Your provider can use the data to help it determine what actions to perform or to maintain additional information. 


### -param pbData [in]

Pointer to the buffer to release.


## -returns



Do not return a value from this function. 




## -remarks



The <b>PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE</b> function is currently called by only the Secure Channel (Schannel) security package. Schannel calls <a href="https://msdn.microsoft.com/2073915D-F23B-41BD-8376-4493FE9D62C6">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_GET</a> to retrieve an object and then calls <b>PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE</b> to remove the data returned by the <b>PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_GET</b> call from memory when it is no longer required.




## -see-also




<a href="https://msdn.microsoft.com/4B319A83-C230-4BFE-AF21-1395ED2D234B">CRYPT_OBJECT_LOCATOR_PROVIDER_TABLE</a>



<a href="https://msdn.microsoft.com/2073915D-F23B-41BD-8376-4493FE9D62C6">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_GET</a>



<a href="https://msdn.microsoft.com/DBDE5B98-AC31-4CA0-A7C6-1FCD8FAC51FC">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE</a>
 

 


---
UID: NC:wincrypt.PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_IDENTIFIER
title: PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_IDENTIFIER
author: windows-sdk-content
description: Releases memory for an object identifier.
old-location: security\pfn_crypt_object_locator_provider_free_identifier.htm
tech.root: seccrypto
ms.assetid: C2ED3B51-8B98-412C-A571-D107F2BEC5F1
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_IDENTIFIER, PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_IDENTIFIER callback, PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_IDENTIFIER callback function [Security], security.pfn_crypt_object_locator_provider_free_identifier, wincrypt/PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_IDENTIFIER
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
 - PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_IDENTIFIER
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_IDENTIFIER callback function


## -description


The <b>PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_IDENTIFIER</b> callback function releases memory for an object identifier.


## -parameters




### -param pPluginContext [in, optional]

Pointer to an optional buffer defined by this provider and returned by the <a href="https://msdn.microsoft.com/DBDE5B98-AC31-4CA0-A7C6-1FCD8FAC51FC">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE</a> function. The buffer is not modified by the caller. Your provider can use the data to help it determine what actions to perform or to maintain additional information. 


### -param pIdentifier [in]

Pointer to the buffer that contains the identifier.


## -returns



Do not return a value from this function. 




## -remarks



The <b>PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_IDENTIFIER</b> function is currently called by only the Secure Channel (Schannel) security package. This function may be called for any of the following reasons:

<ul>
<li>An error occurred when processing the object returned by the <a href="https://msdn.microsoft.com/2073915D-F23B-41BD-8376-4493FE9D62C6">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_GET</a> function.</li>
<li>The object returned by <a href="https://msdn.microsoft.com/2073915D-F23B-41BD-8376-4493FE9D62C6">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_GET</a> is no longer needed.</li>
<li>An updated object has been retrieved and the original object is no longer required.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/4B319A83-C230-4BFE-AF21-1395ED2D234B">CRYPT_OBJECT_LOCATOR_PROVIDER_TABLE</a>



<a href="https://msdn.microsoft.com/2073915D-F23B-41BD-8376-4493FE9D62C6">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_GET</a>



<a href="https://msdn.microsoft.com/DBDE5B98-AC31-4CA0-A7C6-1FCD8FAC51FC">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE</a>
 

 


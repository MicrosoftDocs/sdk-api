---
UID: NS:wincrypt._CRYPT_OBJECT_LOCATOR_PROVIDER_TABLE
title: "_CRYPT_OBJECT_LOCATOR_PROVIDER_TABLE"
author: windows-sdk-content
description: Contains pointers to functions implemented by an object location provider.
old-location: security\crypt_object_locator_provider_table.htm
tech.root: seccrypto
ms.assetid: 4B319A83-C230-4BFE-AF21-1395ED2D234B
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: "*PCRYPT_OBJECT_LOCATOR_PROVIDER_TABLE, CRYPT_OBJECT_LOCATOR_PROVIDER_TABLE, CRYPT_OBJECT_LOCATOR_PROVIDER_TABLE structure [Security], PCRYPT_OBJECT_LOCATOR_PROVIDER_TABLE, PCRYPT_OBJECT_LOCATOR_PROVIDER_TABLE structure pointer [Security], _CRYPT_OBJECT_LOCATOR_PROVIDER_TABLE, security.crypt_object_locator_provider_table, wincrypt/CRYPT_OBJECT_LOCATOR_PROVIDER_TABLE, wincrypt/PCRYPT_OBJECT_LOCATOR_PROVIDER_TABLE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CRYPT_OBJECT_LOCATOR_PROVIDER_TABLE
product: Windows
targetos: Windows
req.typenames: CRYPT_OBJECT_LOCATOR_PROVIDER_TABLE, *PCRYPT_OBJECT_LOCATOR_PROVIDER_TABLE
req.redist: 
---

# _CRYPT_OBJECT_LOCATOR_PROVIDER_TABLE structure


## -description


The <b>CRYPT_OBJECT_LOCATOR_PROVIDER_TABLE</b> structure contains pointers to functions implemented by an object location provider. This structure is used by the <a href="https://msdn.microsoft.com/DBDE5B98-AC31-4CA0-A7C6-1FCD8FAC51FC">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE</a> callback function.


## -struct-fields




### -field cbSize

Size, in bytes, of this structure.


### -field pfnGet

Pointer to the <a href="https://msdn.microsoft.com/2073915D-F23B-41BD-8376-4493FE9D62C6">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_GET</a> function implemented by the provider.


### -field pfnRelease

Pointer to the <a href="https://msdn.microsoft.com/DDF1243D-A6C8-426A-A800-018E7FF7E182">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_RELEASE</a>  function implemented by the provider.


### -field pfnFreePassword

Pointer to the <a href="https://msdn.microsoft.com/C05D5024-9A67-4EA8-9F61-D31AF3AE8545">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_PASSWORD</a>  function implemented by the provider.


### -field pfnFree

Pointer to the <a href="https://msdn.microsoft.com/4C27BF58-79AB-4AD3-8D43-EEE7F73071D2">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE</a>  function implemented by the provider.


### -field pfnFreeIdentifier

Pointer to the <a href="https://msdn.microsoft.com/C2ED3B51-8B98-412C-A571-D107F2BEC5F1">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_IDENTIFIER</a>  function implemented by the provider.


## -remarks



No pointers in this table can be <b>NULL</b>. The client application does not free this structure. It is expected that the provider will return a table that is not allocated on the heap.




## -see-also




<a href="https://msdn.microsoft.com/DBDE5B98-AC31-4CA0-A7C6-1FCD8FAC51FC">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE</a>
 

 


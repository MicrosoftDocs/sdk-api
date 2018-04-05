---
UID: NC:wincrypt.PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FLUSH
title: PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FLUSH
author: windows-driver-content
description: Specifies that an object has changed.
old-location: security\pfn_crypt_object_locator_provider_flush.htm
old-project: SecCrypto
ms.assetid: F6EE5424-A3ED-4E90-897B-56C605EB985C
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FLUSH, PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FLUSH function pointer [Security], security.pfn_crypt_object_locator_provider_flush, wincrypt/PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FLUSH
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
-	PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FLUSH
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FLUSH callback


## -description


The <b>PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FLUSH</b> callback function specifies that an object has changed. The provider calls this function when the provider has determined that a particular name or identifier has been updated.


## -parameters




### -param pContext [in]

Pointer to a provider defined object that contains information about this provider.


### -param *rgIdentifierOrNameList [in]

Pointer to an array of names or identifiers.


### -param dwIdentifierOrNameListCount [in]

The number of names or identifiers specified by the <i>rgIdentifierOrNameList</i> parameter.


## -returns



If the function succeeds, return nonzero (<b>TRUE</b>).

If the function fails, return zero (<b>FALSE</b>). 




## -remarks



A provider calls an implementation of the <b>PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FLUSH</b> callback function to indicate that an object has changed.

A pointer to this function is set in the <i>pfnFlush</i> parameter of the <a href="https://msdn.microsoft.com/DBDE5B98-AC31-4CA0-A7C6-1FCD8FAC51FC">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE</a> function.

An identifier is data chosen by the provider to represent the object being located for the caller. Identifiers need not be unique. If the provider determines that the object associated with the identifier is no longer valid, it should call this function to mark all objects with the associated identifier as invalid. This function is thread safe.




## -see-also




<a href="https://msdn.microsoft.com/DBDE5B98-AC31-4CA0-A7C6-1FCD8FAC51FC">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE</a>
 

 


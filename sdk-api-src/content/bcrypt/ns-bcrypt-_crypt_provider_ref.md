---
UID: NS:bcrypt._CRYPT_PROVIDER_REF
title: "_CRYPT_PROVIDER_REF"
author: windows-driver-content
description: Contains information about a cryptographic interface that a provider supports.
old-location: security\crypt_provider_ref.htm
old-project: SecCNG
ms.assetid: 3bd4a07c-8b80-4bbc-9922-88ea007f6ccd
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: "*PCRYPT_PROVIDER_REF, CRYPT_PROVIDER_REF, CRYPT_PROVIDER_REF structure [Security], PCRYPT_PROVIDER_REF, PCRYPT_PROVIDER_REF structure pointer [Security], _CRYPT_PROVIDER_REF, bcrypt/CRYPT_PROVIDER_REF, bcrypt/PCRYPT_PROVIDER_REF, security.crypt_provider_ref"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: bcrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: CRYPT_PROVIDER_REF, *PCRYPT_PROVIDER_REF
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Bcrypt.h
api_name:
-	CRYPT_PROVIDER_REF
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _CRYPT_PROVIDER_REF structure


## -description


The <b>CRYPT_PROVIDER_REF</b> structure contains information about a cryptographic interface that a provider supports.


## -struct-fields




### -field dwInterface

The identifier of the interface that this reference applies to. This will be one of the <a href="https://msdn.microsoft.com/509c89ff-0c73-4e57-9c39-400522f2086e">CNG Interface Identifiers</a>.


### -field pszFunction

A pointer to a null-terminated Unicode string that identifies the algorithm or function that the reference applies to. This can be one of the standard <a href="https://msdn.microsoft.com/a05ae7e6-d882-4287-9990-23e4cd340b05">CNG Algorithm Identifiers</a> or the identifier for another registered algorithm.


### -field pszProvider

A pointer to a null-terminated Unicode string that contains the name of the provider.


### -field cProperties

The number of elements in the <b>rgpProperties</b> array. If the algorithm or function has no properties, then this member will be zero.


### -field rgpProperties

An array of <a href="https://msdn.microsoft.com/450225b8-87f2-4ce2-853d-e78cf64bd13d">CRYPT_PROPERTY_REF</a> structure pointers that contain the properties for this algorithm or function. The <b>cProperties</b> member contains the number of elements in this array.


### -field pUM

A pointer to a <a href="https://msdn.microsoft.com/fb853879-3ee9-45e7-bab6-31f8f8211680">CRYPT_IMAGE_REF</a> structure that contains information about the user mode provider module. If this information was not requested or the provider is not registered as a user mode provider, this member will be <b>NULL</b>.


### -field pKM

A pointer to a <a href="https://msdn.microsoft.com/fb853879-3ee9-45e7-bab6-31f8f8211680">CRYPT_IMAGE_REF</a> structure that contains information about the kernel mode provider module. If this information was not requested or the provider is not registered as a kernel mode provider, this member will be <b>NULL</b>.


## -see-also




<a href="https://msdn.microsoft.com/cf30f635-4918-4911-9db0-df90d26a2f1a">BCryptResolveProviders</a>



<a href="https://msdn.microsoft.com/e2aaaa02-96e3-4447-b19b-b9db07b49135">CRYPT_PROVIDER_REFS</a>
 

 


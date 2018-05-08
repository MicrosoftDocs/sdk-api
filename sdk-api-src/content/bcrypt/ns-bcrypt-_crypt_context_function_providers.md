---
UID: NS:bcrypt._CRYPT_CONTEXT_FUNCTION_PROVIDERS
title: "_CRYPT_CONTEXT_FUNCTION_PROVIDERS"
author: windows-driver-content
description: Contains a set of cryptographic function providers for a CNG configuration context.
old-location: security\crypt_context_function_providers.htm
old-project: SecCNG
ms.assetid: 5e175ac2-38eb-44c4-a01a-fb436e833546
ms.author: windowsdriverdev
ms.date: 5/1/2018
ms.keywords: "*PCRYPT_CONTEXT_FUNCTION_PROVIDERS, CRYPT_CONTEXT_FUNCTION_PROVIDERS, CRYPT_CONTEXT_FUNCTION_PROVIDERS structure [Security], PCRYPT_CONTEXT_FUNCTION_PROVIDERS, PCRYPT_CONTEXT_FUNCTION_PROVIDERS structure pointer [Security], _CRYPT_CONTEXT_FUNCTION_PROVIDERS, bcrypt/CRYPT_CONTEXT_FUNCTION_PROVIDERS, bcrypt/PCRYPT_CONTEXT_FUNCTION_PROVIDERS, security.crypt_context_function_providers"
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
req.typenames: CRYPT_CONTEXT_FUNCTION_PROVIDERS, *PCRYPT_CONTEXT_FUNCTION_PROVIDERS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Bcrypt.h
api_name:
-	CRYPT_CONTEXT_FUNCTION_PROVIDERS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _CRYPT_CONTEXT_FUNCTION_PROVIDERS structure


## -description


The <b>CRYPT_CONTEXT_FUNCTION_PROVIDERS</b> structure contains a set of cryptographic function providers for a CNG configuration context.


## -struct-fields




### -field cProviders

The number of elements in the <b>rgpszProviders</b> array.


### -field rgpszProviders

An array of pointers to null-terminated Unicode strings that contain the identifiers of the function providers contained in this set. The <b>cProviders</b> member contains the number of elements in this array.


## -see-also




<a href="https://msdn.microsoft.com/82776e61-03bb-463b-8767-fa4f70fe1341">BCryptEnumContextFunctionProviders</a>
 

 


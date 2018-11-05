---
UID: NS:bcrypt._CRYPT_CONTEXT_FUNCTION_PROVIDERS
title: "_CRYPT_CONTEXT_FUNCTION_PROVIDERS"
author: windows-sdk-content
description: Contains a set of cryptographic function providers for a CNG configuration context.
old-location: security\crypt_context_function_providers.htm
tech.root: seccng
ms.assetid: 5e175ac2-38eb-44c4-a01a-fb436e833546
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: "*PCRYPT_CONTEXT_FUNCTION_PROVIDERS, CRYPT_CONTEXT_FUNCTION_PROVIDERS, CRYPT_CONTEXT_FUNCTION_PROVIDERS structure [Security], PCRYPT_CONTEXT_FUNCTION_PROVIDERS, PCRYPT_CONTEXT_FUNCTION_PROVIDERS structure pointer [Security], _CRYPT_CONTEXT_FUNCTION_PROVIDERS, bcrypt/CRYPT_CONTEXT_FUNCTION_PROVIDERS, bcrypt/PCRYPT_CONTEXT_FUNCTION_PROVIDERS, security.crypt_context_function_providers"
ms.prod: windows
ms.technology: windows-sdk
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Bcrypt.h
api_name:
 - CRYPT_CONTEXT_FUNCTION_PROVIDERS
product: Windows
targetos: Windows
req.typenames: CRYPT_CONTEXT_FUNCTION_PROVIDERS, *PCRYPT_CONTEXT_FUNCTION_PROVIDERS
req.redist: 
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




<a href="https://msdn.microsoft.com/en-us/library/Aa375425(v=VS.85).aspx">BCryptEnumContextFunctionProviders</a>
 

 


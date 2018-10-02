---
UID: NS:bcrypt._CRYPT_CONTEXT_FUNCTIONS
title: "_CRYPT_CONTEXT_FUNCTIONS"
author: windows-sdk-content
description: Contains a set of cryptographic functions for a CNG configuration context.
old-location: security\crypt_context_functions.htm
tech.root: SecCNG
ms.assetid: c576f39c-a03a-47aa-90b7-500736070c6f
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PCRYPT_CONTEXT_FUNCTIONS, CRYPT_CONTEXT_FUNCTIONS, CRYPT_CONTEXT_FUNCTIONS structure [Security], PCRYPT_CONTEXT_FUNCTIONS, PCRYPT_CONTEXT_FUNCTIONS structure pointer [Security], _CRYPT_CONTEXT_FUNCTIONS, bcrypt/CRYPT_CONTEXT_FUNCTIONS, bcrypt/PCRYPT_CONTEXT_FUNCTIONS, security.crypt_context_functions"
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
 - CRYPT_CONTEXT_FUNCTIONS
product: Windows
targetos: Windows
req.typenames: CRYPT_CONTEXT_FUNCTIONS, *PCRYPT_CONTEXT_FUNCTIONS
req.redist: 
---

# _CRYPT_CONTEXT_FUNCTIONS structure


## -description


The <b>CRYPT_CONTEXT_FUNCTIONS</b> structure contains a set of cryptographic functions for a CNG configuration context.


## -struct-fields




### -field cFunctions

The number of elements in the <b>rgpszFunctions</b> array.


### -field rgpszFunctions

An array of pointers to null-terminated Unicode strings that contain the identifiers of the cryptographic functions contained in this set. The <b>cFunctions</b> member contains the number of elements in this array.


## -see-also




<a href="https://msdn.microsoft.com/81bdfd47-7001-4e63-a8b3-33dae99f2c66">BCryptEnumContextFunctions</a>
 

 


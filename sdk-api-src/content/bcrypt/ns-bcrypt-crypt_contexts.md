---
UID: NS:bcrypt._CRYPT_CONTEXTS
title: CRYPT_CONTEXTS (bcrypt.h)
author: windows-sdk-content
description: Contains a set of CNG configuration context identifiers.
old-location: security\crypt_contexts.htm
tech.root: SecCNG
ms.assetid: a1b60660-a4c5-4880-8cd4-48d8717c77c3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PCRYPT_CONTEXTS, CRYPT_CONTEXTS, CRYPT_CONTEXTS structure [Security], PCRYPT_CONTEXTS, PCRYPT_CONTEXTS structure pointer [Security], bcrypt/CRYPT_CONTEXTS, bcrypt/PCRYPT_CONTEXTS, security.crypt_contexts"
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
 - CRYPT_CONTEXTS
product: Windows
targetos: Windows
req.typenames: CRYPT_CONTEXTS, *PCRYPT_CONTEXTS
req.redist: 
---

# CRYPT_CONTEXTS structure


## -description


The <b>CRYPT_CONTEXTS</b> structure contains a set of CNG configuration context identifiers.


## -struct-fields




### -field cContexts

Contains the number of elements in the <b>rgpszContexts</b> array.


### -field rgpszContexts

An array of pointers to null-terminated Unicode strings that contain the identifiers of the contexts contained in this set. The <b>cContext</b> member contains the number of elements in this array.


## -see-also




<a href="https://msdn.microsoft.com/02646a80-6e93-4169-83da-0488ff3da56f">BCryptEnumContexts</a>
 

 


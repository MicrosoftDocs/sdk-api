---
UID: NS:bcrypt._CRYPT_PROVIDER_REFS
title: "_CRYPT_PROVIDER_REFS"
author: windows-sdk-content
description: Contains a collection of provider references.
old-location: security\crypt_provider_refs.htm
old-project: seccng
ms.assetid: e2aaaa02-96e3-4447-b19b-b9db07b49135
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: "*PCRYPT_PROVIDER_REFS, CRYPT_PROVIDER_REFS, CRYPT_PROVIDER_REFS structure [Security], PCRYPT_PROVIDER_REFS, PCRYPT_PROVIDER_REFS structure pointer [Security], _CRYPT_PROVIDER_REFS, bcrypt/CRYPT_PROVIDER_REFS, bcrypt/PCRYPT_PROVIDER_REFS, security.crypt_provider_refs"
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
tech.root: 
req.typenames: CRYPT_PROVIDER_REFS, *PCRYPT_PROVIDER_REFS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Bcrypt.h
api_name:
 - CRYPT_PROVIDER_REFS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _CRYPT_PROVIDER_REFS structure


## -description


The <b>CRYPT_PROVIDER_REFS</b> structure contains a collection of provider references.


## -struct-fields




### -field cProviders

The number of elements in the <b>rgpProviders</b> array.


### -field rgpProviders

An array of <a href="https://msdn.microsoft.com/3bd4a07c-8b80-4bbc-9922-88ea007f6ccd">CRYPT_PROVIDER_REF</a> structure pointers that contain the provider references. The <b>cProviders</b> member contains the number of elements in this array.


## -see-also




<a href="https://msdn.microsoft.com/cf30f635-4918-4911-9db0-df90d26a2f1a">BCryptResolveProviders</a>
 

 


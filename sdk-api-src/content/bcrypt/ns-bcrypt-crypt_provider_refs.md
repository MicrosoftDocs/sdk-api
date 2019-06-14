---
UID: NS:bcrypt._CRYPT_PROVIDER_REFS
title: CRYPT_PROVIDER_REFS (bcrypt.h)
author: windows-sdk-content
description: Contains a collection of provider references.
old-location: security\crypt_provider_refs.htm
tech.root: SecCNG
ms.assetid: e2aaaa02-96e3-4447-b19b-b9db07b49135
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PCRYPT_PROVIDER_REFS, CRYPT_PROVIDER_REFS, CRYPT_PROVIDER_REFS structure [Security], PCRYPT_PROVIDER_REFS, PCRYPT_PROVIDER_REFS structure pointer [Security], bcrypt/CRYPT_PROVIDER_REFS, bcrypt/PCRYPT_PROVIDER_REFS, security.crypt_provider_refs"
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
 - CRYPT_PROVIDER_REFS
product: Windows
targetos: Windows
req.typenames: CRYPT_PROVIDER_REFS, *PCRYPT_PROVIDER_REFS
req.redist: 
ms.custom: 19H1
---

# CRYPT_PROVIDER_REFS structure


## -description


The <b>CRYPT_PROVIDER_REFS</b> structure contains a collection of provider references.


## -struct-fields




### -field cProviders

The number of elements in the <b>rgpProviders</b> array.


### -field rgpProviders

An array of <a href="https://docs.microsoft.com/windows/desktop/api/bcrypt/ns-bcrypt-_crypt_provider_ref">CRYPT_PROVIDER_REF</a> structure pointers that contain the provider references. The <b>cProviders</b> member contains the number of elements in this array.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/bcrypt/nf-bcrypt-bcryptresolveproviders">BCryptResolveProviders</a>
 

 


---
UID: NS:ncrypt.NCryptProviderName
title: NCryptProviderName (ncrypt.h)
description: Used to contain the name of a CNG key storage provider.
helpviewer_keywords: ["NCryptProviderName","NCryptProviderName structure [Security]","ncrypt/NCryptProviderName","security.ncryptprovidername_struct"]
old-location: security\ncryptprovidername_struct.htm
tech.root: security
ms.assetid: 21d8bf28-ee3f-4036-b3b0-d9c68cb14fa9
ms.date: 12/05/2018
ms.keywords: NCryptProviderName, NCryptProviderName structure [Security], ncrypt/NCryptProviderName, security.ncryptprovidername_struct
req.header: ncrypt.h
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
targetos: Windows
req.typenames: NCryptProviderName
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NCryptProviderName
 - ncrypt/NCryptProviderName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ncrypt.h
api_name:
 - NCryptProviderName
---

# NCryptProviderName structure


## -description

The <b>NCryptProviderName</b> structure is used to contain the name of a CNG key storage provider. This structure is used with the <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptenumstorageproviders">NCryptEnumStorageProviders</a> function to return the names of the registered CNG key storage providers.

## -struct-fields

### -field pszName

A pointer to a null-terminated Unicode string that contains the name of the provider.

### -field pszComment

A pointer to a null-terminated Unicode string that contains optional text for the provider.

## -see-also

<a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptenumstorageproviders">NCryptEnumStorageProviders</a>
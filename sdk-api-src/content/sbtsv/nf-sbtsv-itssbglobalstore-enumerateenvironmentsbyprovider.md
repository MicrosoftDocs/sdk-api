---
UID: NF:sbtsv.ITsSbGlobalStore.EnumerateEnvironmentsByProvider
title: ITsSbGlobalStore::EnumerateEnvironmentsByProvider (sbtsv.h)
description: Returns an array that contains the environments present on the specified provider.
helpviewer_keywords: ["EnumerateEnvironmentsByProvider","EnumerateEnvironmentsByProvider method [Remote Desktop Services]","EnumerateEnvironmentsByProvider method [Remote Desktop Services]","ITsSbGlobalStore interface","ITsSbGlobalStore interface [Remote Desktop Services]","EnumerateEnvironmentsByProvider method","ITsSbGlobalStore.EnumerateEnvironmentsByProvider","ITsSbGlobalStore::EnumerateEnvironmentsByProvider","sbtsv/ITsSbGlobalStore::EnumerateEnvironmentsByProvider","termserv.itssbglobalstore_enumerateenvironmentsbyprovider"]
old-location: termserv\itssbglobalstore_enumerateenvironmentsbyprovider.htm
tech.root: TermServ
ms.assetid: 4fb29524-61e3-4d1a-be98-45f61b796e9e
ms.date: 12/05/2018
ms.keywords: EnumerateEnvironmentsByProvider, EnumerateEnvironmentsByProvider method [Remote Desktop Services], EnumerateEnvironmentsByProvider method [Remote Desktop Services],ITsSbGlobalStore interface, ITsSbGlobalStore interface [Remote Desktop Services],EnumerateEnvironmentsByProvider method, ITsSbGlobalStore.EnumerateEnvironmentsByProvider, ITsSbGlobalStore::EnumerateEnvironmentsByProvider, sbtsv/ITsSbGlobalStore::EnumerateEnvironmentsByProvider, termserv.itssbglobalstore_enumerateenvironmentsbyprovider
req.header: sbtsv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbtsv.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITsSbGlobalStore::EnumerateEnvironmentsByProvider
 - sbtsv/ITsSbGlobalStore::EnumerateEnvironmentsByProvider
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbGlobalStore.EnumerateEnvironmentsByProvider
---

# ITsSbGlobalStore::EnumerateEnvironmentsByProvider


## -description

Returns an array that contains the environments present on the specified provider.

## -parameters

### -param ProviderName [in]

The name of the provider.

### -param pdwCount [in, out]

A pointer to the number of environments retrieved.

### -param ppVal [out]

A pointer to an array that contains references to the environments present. When you have finished using the array, release each element and free the array by calling the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbglobalstore">ITsSbGlobalStore</a>
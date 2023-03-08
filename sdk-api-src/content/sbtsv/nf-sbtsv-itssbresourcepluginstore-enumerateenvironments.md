---
UID: NF:sbtsv.ITsSbResourcePluginStore.EnumerateEnvironments
title: ITsSbResourcePluginStore::EnumerateEnvironments (sbtsv.h)
description: Returns an array that contains the environments present in the resource plug-in store.
helpviewer_keywords: ["EnumerateEnvironments","EnumerateEnvironments method [Remote Desktop Services]","EnumerateEnvironments method [Remote Desktop Services]","ITsSbResourcePluginStore interface","EnumerateEnvironments method [Remote Desktop Services]","ITsSbResourcePluginStoreEx interface","ITsSbResourcePluginStore interface [Remote Desktop Services]","EnumerateEnvironments method","ITsSbResourcePluginStore.EnumerateEnvironments","ITsSbResourcePluginStore::EnumerateEnvironments","ITsSbResourcePluginStoreEx interface [Remote Desktop Services]","EnumerateEnvironments method","ITsSbResourcePluginStoreEx::EnumerateEnvironments","sbtsv/ITsSbResourcePluginStore::EnumerateEnvironments","sbtsv/ITsSbResourcePluginStoreEx::EnumerateEnvironments","termserv.itssbresourcepluginstore_enumerateenvironments"]
old-location: termserv\itssbresourcepluginstore_enumerateenvironments.htm
tech.root: TermServ
ms.assetid: 5c9d2fb4-05e7-449d-8326-b983701b3302
ms.date: 12/05/2018
ms.keywords: EnumerateEnvironments, EnumerateEnvironments method [Remote Desktop Services], EnumerateEnvironments method [Remote Desktop Services],ITsSbResourcePluginStore interface, EnumerateEnvironments method [Remote Desktop Services],ITsSbResourcePluginStoreEx interface, ITsSbResourcePluginStore interface [Remote Desktop Services],EnumerateEnvironments method, ITsSbResourcePluginStore.EnumerateEnvironments, ITsSbResourcePluginStore::EnumerateEnvironments, ITsSbResourcePluginStoreEx interface [Remote Desktop Services],EnumerateEnvironments method, ITsSbResourcePluginStoreEx::EnumerateEnvironments, sbtsv/ITsSbResourcePluginStore::EnumerateEnvironments, sbtsv/ITsSbResourcePluginStoreEx::EnumerateEnvironments, termserv.itssbresourcepluginstore_enumerateenvironments
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
 - ITsSbResourcePluginStore::EnumerateEnvironments
 - sbtsv/ITsSbResourcePluginStore::EnumerateEnvironments
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
 - ITsSbResourcePluginStore.EnumerateEnvironments
 - ITsSbResourcePluginStoreEx.EnumerateEnvironments
---

# ITsSbResourcePluginStore::EnumerateEnvironments


## -description

Returns an array that contains the environments present in the resource plug-in store.

## -parameters

### -param pdwCount [in, out]

A pointer to the number of targets retrieved.

### -param pVal [out]

A pointer to an array that contains references to the environments present. When you have finished using the array, release each element and free the array by calling the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment">ITsSbEnvironment</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore">ITsSbResourcePluginStore</a>



<a href="/windows/desktop/TermServ/itssbresourcepluginstoreex">ITsSbResourcePluginStoreEx</a>
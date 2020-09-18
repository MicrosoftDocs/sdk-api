---
UID: NF:cscobj.IOfflineFilesCache.GetLocation
title: IOfflineFilesCache::GetLocation (cscobj.h)
description: Retrieves the current fully qualified directory path of the Offline Files cache.
helpviewer_keywords: ["GetLocation","GetLocation method [Offline Files]","GetLocation method [Offline Files]","IOfflineFilesCache interface","IOfflineFilesCache interface [Offline Files]","GetLocation method","IOfflineFilesCache.GetLocation","IOfflineFilesCache::GetLocation","cscobj/IOfflineFilesCache::GetLocation","of.iofflinefilescache_getlocation"]
old-location: of\iofflinefilescache_getlocation.htm
tech.root: of
ms.assetid: e608c662-23d2-4dcc-95fc-e949ba9f848f
ms.date: 12/05/2018
ms.keywords: GetLocation, GetLocation method [Offline Files], GetLocation method [Offline Files],IOfflineFilesCache interface, IOfflineFilesCache interface [Offline Files],GetLocation method, IOfflineFilesCache.GetLocation, IOfflineFilesCache::GetLocation, cscobj/IOfflineFilesCache::GetLocation, of.iofflinefilescache_getlocation
req.header: cscobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOfflineFilesCache::GetLocation
 - cscobj/IOfflineFilesCache::GetLocation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesCache.GetLocation
---

# IOfflineFilesCache::GetLocation


## -description

Retrieves the current fully qualified directory path of the Offline Files cache.

## -parameters

### -param ppszPath [out]

Address of pointer variable to accept the address of a string containing the fully qualified path of the Offline Files cache directory.  Upon successful return, the caller is expected to free the returned buffer by using  the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.

## -returns

Returns <b>S_OK</b> if successful, or an error value otherwise.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilescache">IOfflineFilesCache</a>
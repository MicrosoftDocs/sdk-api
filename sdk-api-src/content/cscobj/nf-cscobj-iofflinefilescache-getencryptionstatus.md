---
UID: NF:cscobj.IOfflineFilesCache.GetEncryptionStatus
title: IOfflineFilesCache::GetEncryptionStatus (cscobj.h)
description: Retrieves the current encryption state (encrypted or unencrypted) of the Offline Files cache.
helpviewer_keywords: ["GetEncryptionStatus","GetEncryptionStatus method [Offline Files]","GetEncryptionStatus method [Offline Files]","IOfflineFilesCache interface","IOfflineFilesCache interface [Offline Files]","GetEncryptionStatus method","IOfflineFilesCache.GetEncryptionStatus","IOfflineFilesCache::GetEncryptionStatus","cscobj/IOfflineFilesCache::GetEncryptionStatus","of.iofflinefilescache_getencryptionstatus"]
old-location: of\iofflinefilescache_getencryptionstatus.htm
tech.root: of
ms.assetid: 87c2aced-84c9-40cb-bdf2-6974925e89d5
ms.date: 12/05/2018
ms.keywords: GetEncryptionStatus, GetEncryptionStatus method [Offline Files], GetEncryptionStatus method [Offline Files],IOfflineFilesCache interface, IOfflineFilesCache interface [Offline Files],GetEncryptionStatus method, IOfflineFilesCache.GetEncryptionStatus, IOfflineFilesCache::GetEncryptionStatus, cscobj/IOfflineFilesCache::GetEncryptionStatus, of.iofflinefilescache_getencryptionstatus
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
 - IOfflineFilesCache::GetEncryptionStatus
 - cscobj/IOfflineFilesCache::GetEncryptionStatus
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
 - IOfflineFilesCache.GetEncryptionStatus
---

# IOfflineFilesCache::GetEncryptionStatus


## -description

Retrieves the current encryption state (encrypted or unencrypted) of the Offline Files cache.

## -parameters

### -param pbEncrypted [out]

Receives <b>TRUE</b> if the Offline Files cache is configured to be encrypted; <b>FALSE</b> if configured to be unencrypted.

### -param pbPartial [out]

Receives <b>TRUE</b> if the Offline Files cache is partially encrypted or partially unencrypted based on the value returned in <i>pbEncrypted</i>; <b>FALSE</b> if it is fully encrypted or unencrypted.

## -returns

Returns <b>S_OK</b> if successful, or an error value otherwise.

## -remarks

This encryption state is read from the Offline Files cache and reflects the state of the cache at that instant.

This method returns two values that indicate if the cache is fully encrypted, partially encrypted, fully unencrypted or partially unencrypted.

To change the encryption state of the cache, use the <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilescache-encrypt">IOfflineFilesCache::Encrypt</a> method.


#### Examples

The following example shows how to use this method.


```cpp
    //
    // Assume we already have a cache ptr.
    //
    IOfflineFilesCache *pCache;
    BOOL bEncrypted;
    BOOL bPartial;
    HRESULT hr = pCache->GetEncryptionStatus(&bEncrypted, &bPartial);
    if (SUCCEEDED(hr))
    {
        if (bEncrypted)
        {
            if (bPartial)
            {
                // Cache is partially encrypted.
            }
            else
            {
                // Cache is fully encrypted.
            }
        }
        else
        {
            if (bPartial)
            {
                // Cache is partially unencrypted.
            }
            else
            {
                // Cache is fully unencrypted.
            }
        }
    }

```

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilescache">IOfflineFilesCache</a>
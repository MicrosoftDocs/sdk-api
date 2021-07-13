---
UID: NF:objidl.IStorage.Revert
title: IStorage::Revert (objidl.h)
description: The Revert method discards all changes that have been made to the storage object since the last commit operation.
helpviewer_keywords: ["IStorage interface [Structured Storage]","Revert method","IStorage.Revert","IStorage::Revert","Revert","Revert method [Structured Storage]","Revert method [Structured Storage]","IStorage interface","_stg_istorage_revert","objidl/IStorage::Revert","stg.istorage_revert"]
old-location: stg\istorage_revert.htm
tech.root: Stg
ms.assetid: d1b7626e-bad1-47b5-8bcd-3da3b05c53c4
ms.date: 12/05/2018
ms.keywords: IStorage interface [Structured Storage],Revert method, IStorage.Revert, IStorage::Revert, Revert, Revert method [Structured Storage], Revert method [Structured Storage],IStorage interface, _stg_istorage_revert, objidl/IStorage::Revert, stg.istorage_revert
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IStorage::Revert
 - objidl/IStorage::Revert
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - IStorage.Revert
---

# IStorage::Revert


## -description

The <b>Revert</b> method discards all changes that have been made to the storage object since the last commit operation.



## -returns

This method can return one of these values.

| Return code | Description |
|----------------|---------------|
|S_OK | The revert operation was successful.|
|E_PENDING | Asynchronous Storage only: Part or all of the storage's data is currently unavailable. |
|STG_E_INSUFFICIENTMEMORY | The revert operation could not be completed due to a lack of memory.|
|STG_E_TOOMANYOPENFILES | The revert operation could not be completed because there are too many open files.|
|STG_E_REVERTED | The storage object has been invalidated by a revert operation above it in the transaction tree.|

## -remarks

For storage objects opened in transacted mode, the <b>IStorage::Revert</b> method discards any uncommitted changes to this storage object or changes that have been committed to this storage object from nested elements.

After this method returns, any existing elements (substorages or streams) that were opened from the reverted storage object are invalid and can no longer be used. Specifying these reverted elements in any call except <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> returns the error STG_E_REVERTED

This method has no effect on storage objects opened in direct mode.

## -see-also

<a href="/windows/desktop/Stg/istorage-compound-file-implementation">IStorage - Compound File Implementation</a>



<a href="/windows/desktop/api/objidl/nf-objidl-istorage-commit">IStorage::Commit</a>

---
UID: NF:objidl.IStorage.SetClass
title: IStorage::SetClass (objidl.h)
description: The SetClass method assigns the specified class identifier (CLSID) to this storage object.
helpviewer_keywords: ["IStorage interface [Structured Storage]","SetClass method","IStorage.SetClass","IStorage::SetClass","SetClass","SetClass method [Structured Storage]","SetClass method [Structured Storage]","IStorage interface","_stg_istorage_setclass","objidl/IStorage::SetClass","stg.istorage_setclass"]
old-location: stg\istorage_setclass.htm
tech.root: Stg
ms.assetid: 02ab2708-fc8b-4941-939a-a819cf823108
ms.date: 12/05/2018
ms.keywords: IStorage interface [Structured Storage],SetClass method, IStorage.SetClass, IStorage::SetClass, SetClass, SetClass method [Structured Storage], SetClass method [Structured Storage],IStorage interface, _stg_istorage_setclass, objidl/IStorage::SetClass, stg.istorage_setclass
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
 - IStorage::SetClass
 - objidl/IStorage::SetClass
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
 - IStorage.SetClass
---

# IStorage::SetClass


## -description

The <b>SetClass</b> method assigns the specified class identifier (CLSID) to this storage object.

## -parameters

### -param clsid [in]

The CLSID that is to be associated with the storage object.

## -returns

This method can return one of these values.

| Return code | Description |
|----------------|---------------|
|S_OK | The CLSID was successfully assigned.|
|E_PENDING | Asynchronous Storage only: Part or all of the storage's data is currently unavailable.|
|STG_E_ACCESSDENIED | The caller does not have enough permissions for assigning a CLSID to the storage object.|
|STG_E_MEDIUMFULL | Not enough space was left on device to complete the operation.|
|STG_E_REVERTED | The storage object has been invalidated by a revert operation above it in the transaction tree.|

## -remarks

When first created, a storage object has an associated CLSID of CLSID_NULL. Call <b>SetClass</b> to assign a CLSID to the storage object.

Call the 
<a href="/windows/desktop/api/objidl/nf-objidl-istorage-stat">IStorage::Stat</a> method to retrieve the current CLSID of a storage object.

## -see-also

<a href="/windows/desktop/Stg/istorage-compound-file-implementation">IStorage - Compound File Implementation</a>



<a href="/windows/desktop/api/objidl/nf-objidl-istorage-stat">IStorage::Stat</a>
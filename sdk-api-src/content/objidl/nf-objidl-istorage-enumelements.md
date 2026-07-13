---
UID: NF:objidl.IStorage.EnumElements
title: IStorage::EnumElements (objidl.h)
description: The EnumElements method retrieves a pointer to an enumerator object that can be used to enumerate the storage and stream objects contained within this storage object.
helpviewer_keywords: ["EnumElements","EnumElements method [Structured Storage]","EnumElements method [Structured Storage]","IStorage interface","IStorage interface [Structured Storage]","EnumElements method","IStorage.EnumElements","IStorage::EnumElements","_stg_istorage_enumelements","objidl/IStorage::EnumElements","stg.istorage_enumelements"]
old-location: stg\istorage_enumelements.htm
tech.root: Stg
ms.assetid: 29ca157e-40e2-4e9a-95fb-a31bb45570f2
ms.date: 12/05/2018
ms.keywords: EnumElements, EnumElements method [Structured Storage], EnumElements method [Structured Storage],IStorage interface, IStorage interface [Structured Storage],EnumElements method, IStorage.EnumElements, IStorage::EnumElements, _stg_istorage_enumelements, objidl/IStorage::EnumElements, stg.istorage_enumelements
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
 - IStorage::EnumElements
 - objidl/IStorage::EnumElements
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
 - IStorage.EnumElements
---

# IStorage::EnumElements


## -description

The <b>EnumElements</b> method retrieves a pointer to an enumerator object that can be used to enumerate the storage and stream objects contained within this storage object.

## -parameters

### -param reserved1 [in]

Reserved for future use; must be zero.

### -param reserved2 [in]

Reserved for future use; must be <b>NULL</b>.

### -param reserved3 [in]

Reserved for future use; must be zero.

### -param ppenum [out]

Pointer to 
<a href="/windows/desktop/api/objidl/nn-objidl-ienumstatstg">IEnumSTATSTG</a>* pointer variable that receives the interface pointer to the new enumerator object.

## -returns

This method can return one of these values.

| Return code | Description |
|----------------|---------------|
|S_OK | The enumerator object was successfully returned.|
|E_PENDING | Asynchronous Storage only: Part or all of the element's data is currently unavailable.|
|STG_E_INSUFFICIENTMEMORY | The enumerator object could not be created due to lack of memory.|
|STG_E_INVALIDPARAMETER | One of the parameters was not valid.|
|STG_E_REVERTED | The storage object has been invalidated by a revert operation above it in the transaction tree.|

## -remarks

The enumerator object returned by this method implements the 
<a href="/windows/desktop/api/objidl/nn-objidl-ienumstatstg">IEnumSTATSTG</a> interface, one of the standard enumerator interfaces that contain the <b>Next</b>, <b>Reset</b>, 
<b>Clone</b>, and <b>Skip</b> methods. 
<b>IEnumSTATSTG</b> enumerates the data stored in an array of 
<a href="/windows/desktop/api/objidl/ns-objidl-statstg">STATSTG</a> structures.

The storage object must be open in read mode to allow the enumeration of its elements.

The enumerator object is permitted to enumerate the elements in any order.
The enumerator object is also permitted to treat the enumeration as a snapshot
or to have the enumeration reflect the current state of the storage object.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-ienumstatstg">IEnumSTATSTG</a>



<a href="/windows/desktop/Stg/istorage-compound-file-implementation">IStorage - Compound File Implementation</a>



<a href="/windows/desktop/api/objidl/ns-objidl-statstg">STATSTG</a>
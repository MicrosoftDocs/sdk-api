---
UID: NF:objidl.IStorage.SetStateBits
title: IStorage::SetStateBits (objidl.h)
description: The SetStateBits method stores up to 32 bits of state information in this storage object.
helpviewer_keywords: ["IStorage interface [Structured Storage]","SetStateBits method","IStorage.SetStateBits","IStorage::SetStateBits","SetStateBits","SetStateBits method [Structured Storage]","SetStateBits method [Structured Storage]","IStorage interface","_stg_istorage_setstatebits","objidl/IStorage::SetStateBits","stg.istorage_setstatebits"]
old-location: stg\istorage_setstatebits.htm
tech.root: Stg
ms.assetid: 52606df8-10ea-40e7-bb61-c86c7b7262d2
ms.date: 12/05/2018
ms.keywords: IStorage interface [Structured Storage],SetStateBits method, IStorage.SetStateBits, IStorage::SetStateBits, SetStateBits, SetStateBits method [Structured Storage], SetStateBits method [Structured Storage],IStorage interface, _stg_istorage_setstatebits, objidl/IStorage::SetStateBits, stg.istorage_setstatebits
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
 - IStorage::SetStateBits
 - objidl/IStorage::SetStateBits
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
 - IStorage.SetStateBits
---

# IStorage::SetStateBits


## -description

The <b>SetStateBits</b> method stores up to 32 bits of state information in this storage object. This method is reserved for future use.

## -parameters

### -param grfStateBits [in]

Specifies the new values of the bits to set. No legal values are defined for these bits; they are all reserved for future use and must not be used by applications.

### -param grfMask [in]

A binary mask indicating which bits in <i>grfStateBits</i> are significant in this call.

## -returns

This method can return one of these values.

| Return code | Description |
|----------------|---------------|
|S_OK | The state information was successfully set.|
|E_PENDING | Asynchronous Storage only: Part or all of the storage's data is currently unavailable. |
|STG_E_ACCESSDENIED | The caller does not have enough permissions for changing this storage object.|
|STG_E_INVALIDFLAG | The value for the grfStateBits or *grfMask* parameter is not valid.|
|STG_E_INVALIDPARAMETER | One of the parameters was not valid.|

## -remarks

The values for the state bits are not currently defined.

## -see-also

<a href="/windows/desktop/Stg/istorage-compound-file-implementation">IStorage - Compound File Implementation</a>



<a href="/windows/desktop/api/objidl/nf-objidl-istorage-stat">IStorage::Stat</a>
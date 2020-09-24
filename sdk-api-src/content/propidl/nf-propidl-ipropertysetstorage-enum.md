---
UID: NF:propidl.IPropertySetStorage.Enum
title: IPropertySetStorage::Enum (propidl.h)
description: The Enum method creates an enumerator object which contains information on the property sets stored in this property set storage. On return, this method supplies a pointer to the IEnumSTATPROPSETSTG pointer on the enumerator object.
helpviewer_keywords: ["Enum","Enum method [Structured Storage]","Enum method [Structured Storage]","IPropertySetStorage interface","IPropertySetStorage [Strctd Stg]","Enum","IPropertySetStorage interface [Structured Storage]","Enum method","IPropertySetStorage.Enum","IPropertySetStorage::Enum","_stg_ipropertysetstorage_enum","propidl/IPropertySetStorage::Enum","stg.ipropertysetstorage_enum"]
old-location: stg\ipropertysetstorage_enum.htm
tech.root: Stg
ms.assetid: 979ee86b-fabc-428c-8134-f16c2a33270f
ms.date: 12/05/2018
ms.keywords: Enum, Enum method [Structured Storage], Enum method [Structured Storage],IPropertySetStorage interface, IPropertySetStorage [Strctd Stg],Enum, IPropertySetStorage interface [Structured Storage],Enum method, IPropertySetStorage.Enum, IPropertySetStorage::Enum, _stg_ipropertysetstorage_enum, propidl/IPropertySetStorage::Enum, stg.ipropertysetstorage_enum
req.header: propidl.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IPropertySetStorage::Enum
 - propidl/IPropertySetStorage::Enum
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
 - IPropertySetStorage.Enum
---

# IPropertySetStorage::Enum


## -description

The <b>Enum</b> method creates an enumerator object which contains information on the property sets stored in this property set storage. On return, this method supplies a pointer to the 
<a href="/windows/desktop/api/propidl/nn-propidl-ienumstatpropsetstg">IEnumSTATPROPSETSTG</a> pointer on the enumerator object.

## -parameters

### -param ppenum [out]

Pointer to 
<a href="/windows/desktop/api/propidl/nn-propidl-ienumstatpropsetstg">IEnumSTATPROPSETSTG</a> pointer variable that receives the interface pointer to the newly created enumerator object.

## -returns

This method can return one of these values.

## -remarks

<b>IPropertySetStorage::Enum</b> creates an enumerator object that can be used to iterate through 
<a href="/windows/desktop/api/propidl/ns-propidl-statpropsetstg">STATPROPSETSTG</a> structures. These sometimes provide information on the property sets managed by 
<a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage">IPropertySetStorage</a>. This method, on return, supplies a pointer to the 
<a href="/windows/desktop/api/propidl/nn-propidl-ienumstatpropsetstg">IEnumSTATPROPSETSTG</a> interface on this enumerator object on return.

## -see-also

<a href="/windows/desktop/Stg/enumall-sample">EnumAll Sample</a>



<a href="/windows/desktop/api/propidl/nn-propidl-ienumstatpropsetstg">IEnumSTATPROPSETSTG</a>



<a href="/windows/desktop/Stg/ienumstatpropsetstg-compound-file-implementation">IEnumSTATPROPSETSTG - Compound File Implementation</a>



<a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage">IPropertySetStorage</a>



<a href="/windows/desktop/Stg/samples">Samples</a>
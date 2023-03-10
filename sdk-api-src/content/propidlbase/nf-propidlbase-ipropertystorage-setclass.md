---
UID: NF:propidlbase.IPropertyStorage.SetClass
title: IPropertyStorage::SetClass (propidlbase.h)
description: The IPropertyStorage::SetClass method assigns a new CLSID to the current property storage object, and persistently stores the CLSID with the object.
helpviewer_keywords: ["IPropertyStorage [Strctd Stg]","SetClass","IPropertyStorage interface [Structured Storage]","SetClass method","IPropertyStorage.SetClass","IPropertyStorage::SetClass","SetClass","SetClass method [Structured Storage]","SetClass method [Structured Storage]","IPropertyStorage interface","_stg_ipropertystorage_setclass","propidl/IPropertyStorage::SetClass","stg.ipropertystorage_setclass"]
old-location: stg\ipropertystorage_setclass.htm
tech.root: Stg
ms.assetid: 88c916e5-b7f0-4f4d-b049-df2b0e1c2423
ms.date: 08/02/2022
ms.keywords: IPropertyStorage [Strctd Stg],SetClass, IPropertyStorage interface [Structured Storage],SetClass method, IPropertyStorage.SetClass, IPropertyStorage::SetClass, SetClass, SetClass method [Structured Storage], SetClass method [Structured Storage],IPropertyStorage interface, _stg_ipropertystorage_setclass, propidl/IPropertyStorage::SetClass, stg.ipropertystorage_setclass
req.header: propidlbase.h
req.include-header: Objbase.h, Propidlbase.h
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
 - IPropertyStorage::SetClass
 - propidlbase/IPropertyStorage::SetClass
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
 - IPropertyStorage.SetClass
---

# IPropertyStorage::SetClass


## -description

The <b>SetClass</b> method assigns a new CLSID to the current property storage object, and persistently stores the CLSID with the object.

## -parameters

### -param clsid [in]

New CLSID to be associated with the property set.

## -returns

This method supports the standard return value E_UNEXPECTED, in addition to the following:

## -remarks

Assigns a CLSID to the current property storage object. The CLSID has no relationship to the stored property IDs. Assigning a CLSID allows a piece of code to be associated with a given instance of a property set; such code, for example, might manage the user interface (UI). Different CLSIDs can be associated with different property set instances that have the same FMTID.

If the property set is created with the <i>pclsid</i> parameter of the <a href="/windows/desktop/api/propidl/nf-propidl-ipropertysetstorage-create">IPropertySetStorage::Create</a> method specified as <b>NULL</b>, the CLSID is set to all zeroes.

The current CLSID on a property storage object can be retrieved with a call to 
<a href="/windows/desktop/api/propidl/nf-propidl-ipropertystorage-stat">IPropertyStorage::Stat</a>. The initial value for the CLSID can be specified at the time that the storage is created with a call to <a href="/windows/desktop/api/propidl/nf-propidl-ipropertysetstorage-create">IPropertySetStorage::Create</a>.

Setting the CLSID on a nonsimple property set (one that can legally contain storage- or stream-valued properties, as described in <a href="/windows/desktop/api/propidl/nf-propidl-ipropertysetstorage-create">IPropertySetStorage::Create</a>) also sets the CLSID on the underlying sub-storage.

## -see-also

<a href="/windows/desktop/api/propidl/nf-propidl-ipropertysetstorage-create">IPropertySetStorage::Create</a>



<a href="/windows/desktop/api/propidl/nn-propidl-ipropertystorage">IPropertyStorage</a>



<a href="/windows/desktop/api/propidl/nf-propidl-ipropertystorage-stat">IPropertyStorage::Stat</a>

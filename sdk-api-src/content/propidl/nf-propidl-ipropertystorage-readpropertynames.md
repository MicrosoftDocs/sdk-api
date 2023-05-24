---
UID: NF:propidl.IPropertyStorage.ReadPropertyNames
title: IPropertyStorage::ReadPropertyNames (propidl.h)
description: The IPropertyStorage::ReadPropertyNames method retrieves any existing string names for the specified property IDs.
helpviewer_keywords: ["IPropertyStorage [Strctd Stg]","IPropertyStorage [Strctd Stg]","ReadPropertyNames","IPropertyStorage interface [Structured Storage]","ReadPropertyNames method","IPropertyStorage.ReadPropertyNames","IPropertyStorage::ReadPropertyNames","ReadPropertyNames","ReadPropertyNames method [Structured Storage]","ReadPropertyNames method [Structured Storage]","IPropertyStorage interface","_stg_ipropertystorage_readpropertynames","propidl/IPropertyStorage::ReadPropertyNames","stg.ipropertystorage_readpropertynames"]
old-location: stg\ipropertystorage_readpropertynames.htm
tech.root: Stg
ms.assetid: 42b0bf7e-0402-425c-8a5f-09eaa16d93fe
ms.date: 08/02/2022
ms.keywords: IPropertyStorage [Strctd Stg], IPropertyStorage [Strctd Stg],ReadPropertyNames, IPropertyStorage interface [Structured Storage],ReadPropertyNames method, IPropertyStorage.ReadPropertyNames, IPropertyStorage::ReadPropertyNames, ReadPropertyNames, ReadPropertyNames method [Structured Storage], ReadPropertyNames method [Structured Storage],IPropertyStorage interface, _stg_ipropertystorage_readpropertynames, propidl/IPropertyStorage::ReadPropertyNames, stg.ipropertystorage_readpropertynames
req.header: propidl.h
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
 - IPropertyStorage::ReadPropertyNames
 - propidl/IPropertyStorage::ReadPropertyNames
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
 - IPropertyStorage.ReadPropertyNames
---

# IPropertyStorage::ReadPropertyNames


## -description

The <b>ReadPropertyNames</b> method retrieves any existing string names for the specified property IDs.

## -parameters

### -param cpropid [in]

The number of elements on input of the array <i>rgpropid</i>.  The value of this parameter can be set to zero, however that defeats the purpose of this method as no property names are thereby read.

### -param rgpropid [in]

An array of property IDs for which names are to be retrieved.

### -param rglpwstrName [in, out]

A caller-allocated array of size <i>cpropid</i> of <b>LPWSTR</b> members. On return, the implementation fills in this array. A given entry contains either the corresponding string name of a property ID or it can be empty if the property ID has no string names.

Each <b>LPWSTR</b> member of the array should be freed using the 
<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.

## -returns

This method supports the standard return value E_UNEXPECTED, in addition to the following:

## -remarks

For each property ID in the list of property IDs supplied in the <i>rgpropid</i> array, <b>ReadPropertyNames</b> retrieves the corresponding string name, if there is one. String names are created either by specifying the names in calls to 
<a href="/windows/desktop/api/propidl/nf-propidl-ipropertystorage-writemultiple">IPropertyStorage::WriteMultiple</a> when creating the property, or through a call to <a href="/windows/desktop/api/propidl/nf-propidl-ipropertystorage-writepropertynames">IPropertyStorage::WritePropertyNames</a>. In either case, the string name is optional, however all properties must have a property ID.

String names mapped to property IDs must be unique within the set.

## -see-also

<a href="/windows/desktop/api/propidl/nn-propidl-ipropertystorage">IPropertyStorage</a>



<a href="/windows/desktop/api/propidl/nf-propidl-ipropertystorage-writemultiple">IPropertyStorage::WriteMultiple</a>



<a href="/windows/desktop/api/propidl/nf-propidl-ipropertystorage-writepropertynames">IPropertyStorage::WritePropertyNames</a>

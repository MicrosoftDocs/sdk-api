---
UID: NF:propidlbase.IPropertyStorage.WritePropertyNames
title: IPropertyStorage::WritePropertyNames (propidlbase.h)
description: The IPropertyStorage::WritePropertyNames method assigns string IPropertyStoragenames to a specified array of property IDs in the current property set.  
helpviewer_keywords: ["IPropertyStorage interface [Structured Storage]","WritePropertyNames method","IPropertyStorage.WritePropertyNames","IPropertyStorage::WritePropertyNames","WritePropertyNames","WritePropertyNames method [Structured Storage]","WritePropertyNames method [Structured Storage]","IPropertyStorage interface","_stg_ipropertystorage_writepropertynames","propidl/IPropertyStorage::WritePropertyNames","stg.ipropertystorage_writepropertynames"]
old-location: stg\ipropertystorage_writepropertynames.htm
tech.root: Stg
ms.assetid: 3612bf29-344a-4389-bd3b-56b9fa297362
ms.date: 08/02/2022
ms.keywords: IPropertyStorage interface [Structured Storage],WritePropertyNames method, IPropertyStorage.WritePropertyNames, IPropertyStorage::WritePropertyNames, WritePropertyNames, WritePropertyNames method [Structured Storage], WritePropertyNames method [Structured Storage],IPropertyStorage interface, _stg_ipropertystorage_writepropertynames, propidl/IPropertyStorage::WritePropertyNames, stg.ipropertystorage_writepropertynames
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
 - IPropertyStorage::WritePropertyNames
 - propidlbase/IPropertyStorage::WritePropertyNames
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
 - IPropertyStorage.WritePropertyNames
---

# IPropertyStorage::WritePropertyNames


## -description

The 
<b>WritePropertyNames</b> method
			assigns string <a href="/windows/desktop/api/propidl/nn-propidl-ipropertystorage">IPropertyStorage</a> names to a specified array of property IDs in the current property set.

## -parameters

### -param cpropid [in]

The size on input of the array <i>rgpropid</i>. Can be zero.  However, making it zero causes this method to become non-operational.

### -param rgpropid [in]

An array of the property IDs for which names are to be set.

### -param rglpwstrName [in]

An array of new names to be assigned to the corresponding property IDs in the <i>rgpropid</i> array. These names may not exceed 255 characters (not including the <b>NULL</b> terminator).

## -returns

This method supports the standard return value <b>E_UNEXPECTED</b>, in addition to the following:

## -remarks

For more information about property sets and memory management, see 
<a href="/windows/desktop/Stg/managing-property-sets">Managing Property Sets</a>.

<b>IPropertyStorage::WritePropertyNames</b> assigns string names to property IDs passed to the method in the <i>rgpropid</i> array. It associates each string name in the <i>rglpwstrName</i> array with the respective property ID in <i>rgpropid</i>. It is explicitly valid to define a name for a property ID that is not currently present in the property storage object.

It is also valid to change the mapping for an existing string name (determined by a case-insensitive match). That is, you can use the 
<b>WritePropertyNames</b> method to map an existing name to a new property ID, or to map a new name to a property ID that already has a name in the dictionary. In either case, the original mapping is deleted. Property names must be unique (as are property IDs) within the property set.

The storage of string property names preserves the case. Unless <b>PROPSETFLAG_CASE_SENSITIVE</b> is passed to 
<a href="/windows/desktop/api/propidl/nf-propidl-ipropertysetstorage-create">IPropertySetStorage::Create</a>, property set names are case insensitive by default. With case-insensitive property sets, the name strings passed by the caller are interpreted according to the locale of the property set, as specified by the <b>PID_LOCALE</b> property. If the property set has no locale property, the current user is assumed by default. String property names are limited in length to 128 characters. Property names that begin with the binary Unicode characters 0x0001 through 0x001F are reserved for future use.

If the value of an element in the <i>rgpropid</i> array parameter is set to 0xffffffff (PID_ILLEGAL), the corresponding name is ignored by <b>IPropertyStorage::WritePropertyNames</b>. For example, if this method is called with a <i>cpropid</i> parameter of 3, but the first element of the array, <i>rgpropid[1]</i>, is set to <b>PID_ILLEGAL</b>, then only two property names are written. The <i>rgpropid[1]</i> element is ignored.

## -see-also

<a href="/windows/desktop/api/propidl/nn-propidl-ipropertystorage">IPropertyStorage</a>



<a href="/windows/desktop/api/propidl/nf-propidl-ipropertystorage-readmultiple">IPropertyStorage::ReadMultiple</a>



<a href="/windows/desktop/api/propidl/nf-propidl-ipropertystorage-readpropertynames">IPropertyStorage::ReadPropertyNames</a>



<a href="/windows/desktop/api/propidl/nf-propidl-ipropertystorage-writemultiple">IPropertyStorage::WriteMultiple</a>



<a href="/windows/desktop/Stg/samples">Samples</a>



<a href="/windows/desktop/Stg/writeread-sample">WriteRead Sample</a>

---
UID: NF:propidl.IPropertyStorage.ReadMultiple
title: IPropertyStorage::ReadMultiple (propidl.h)
description: The IPropertyStorage::ReadMultiple method reads specified properties from the current property set.
helpviewer_keywords: ["IPropertyStorage [Strctd Stg]","ReadMultiple","IPropertyStorage interface [Structured Storage]","ReadMultiple method","IPropertyStorage.ReadMultiple","IPropertyStorage::ReadMultiple","ReadMultiple","ReadMultiple method [Structured Storage]","ReadMultiple method [Structured Storage]","IPropertyStorage interface","_stg_ipropertystorage_readmultiple","propidl/IPropertyStorage::ReadMultiple","stg.ipropertystorage_readmultiple"]
old-location: stg\ipropertystorage_readmultiple.htm
tech.root: Stg
ms.assetid: a3d708fe-53af-4f1b-94ac-edc40d59a034
ms.date: 08/02/2022
ms.keywords: IPropertyStorage [Strctd Stg],ReadMultiple, IPropertyStorage interface [Structured Storage],ReadMultiple method, IPropertyStorage.ReadMultiple, IPropertyStorage::ReadMultiple, ReadMultiple, ReadMultiple method [Structured Storage], ReadMultiple method [Structured Storage],IPropertyStorage interface, _stg_ipropertystorage_readmultiple, propidl/IPropertyStorage::ReadMultiple, stg.ipropertystorage_readmultiple
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
 - IPropertyStorage::ReadMultiple
 - propidl/IPropertyStorage::ReadMultiple
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
 - IPropertyStorage.ReadMultiple
---

# IPropertyStorage::ReadMultiple


## -description

The
		<b>ReadMultiple</b> method
			 reads specified properties from the current property set.

## -parameters

### -param cpspec [in]

The numeric count of properties to be specified in the <i>rgpspec</i> array. The value of this parameter can  be set to zero; however, that defeats the purpose of the method as no properties are thereby read, regardless of the values set in <i>rgpspec</i>.

### -param rgpspec [in]

An array of 
<a href="/windows/desktop/api/propidl/ns-propidl-propspec">PROPSPEC</a> structures specifies which properties are  read. Properties can be specified either by a property ID or by an optional string name. It is not necessary to specify properties in any particular order in the array. The array can contain duplicate properties, resulting in duplicate property values on return for simple properties. Nonsimple properties should return access denied on an attempt to open them a second time. The array can contain a mixture of property IDs and string IDs.

### -param rgpropvar [out]

Caller-allocated array of a 
<a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure that, on return, contains the values of the properties specified by the corresponding elements in the <i>rgpspec</i> array. The array must be at least large enough to hold values of the <i>cpspec</i> parameter of the 
<b>PROPVARIANT</b> structure. The <i>cpspec</i> parameter specifies the number of properties set in the array. The caller is not required to initialize these 
<b>PROPVARIANT</b> structure values in any specific  order. However, the implementation must fill all members correctly on return. If there is no other appropriate value, the implementation must set the <b>vt</b> member of each 
<b>PROPVARIANT</b> structure to <b>VT_EMPTY</b>.

## -returns

This method supports the standard return value <b>E_UNEXPECTED</b>, as well as the following:

This function can also return any file system errors or Win32 errors wrapped in an <b>HRESULT</b> data type. For more information, see 
<a href="/windows/desktop/com/error-handling-strategies">Error Handling Strategies</a>.

For more information, see 
<a href="/windows/desktop/Stg/property-storage-considerations">Property Storage Considerations</a>.

## -see-also

<a href="/windows/desktop/Stg/enumall-sample">EnumAll Sample</a>



<a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage">IPropertySetStorage</a>



<a href="/windows/desktop/api/propidl/nn-propidl-ipropertystorage">IPropertyStorage</a>



<a href="/windows/desktop/api/propidl/nf-propidl-ipropertystorage-writemultiple">IPropertyStorage::WriteMultiple</a>



<a href="/windows/desktop/api/propidl/nf-propidl-ipropertystorage-writepropertynames">IPropertyStorage::WritePropertyNames</a>



<a href="/windows/desktop/Stg/samples">Samples</a>



<a href="/windows/desktop/Stg/stgcreatepropsetstg-sample">StgCreatePropSetStg Sample</a>



<a href="/windows/desktop/Stg/writeread-sample">WriteRead Sample</a>

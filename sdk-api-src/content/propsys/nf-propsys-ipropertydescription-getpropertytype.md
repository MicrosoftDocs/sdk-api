---
UID: NF:propsys.IPropertyDescription.GetPropertyType
title: IPropertyDescription::GetPropertyType (propsys.h)
description: Gets the variant type of the property.
old-location: properties\IPropertyDescription_GetPropertyType.htm
tech.root: properties
ms.assetid: 88f960b0-4b83-48d9-af24-ad6995ade550
ms.date: 12/05/2018
ms.keywords: GetPropertyType, GetPropertyType method [Windows Properties], GetPropertyType method [Windows Properties],IPropertyDescription interface, IPropertyDescription interface [Windows Properties],GetPropertyType method, IPropertyDescription.GetPropertyType, IPropertyDescription::GetPropertyType, VT_BLOB, VT_BOOL, VT_CLSID, VT_FILETIME, VT_I2, VT_I4, VT_I8, VT_LPWSTR, VT_NULL, VT_R8, VT_STREAM, VT_UI1, VT_UI2, VT_UI4, VT_UI8, VT_UNKNOWN, properties.IPropertyDescription_GetPropertyType, propsys/IPropertyDescription::GetPropertyType, shell.IPropertyDescription_GetPropertyType, shell_IPropertyDescription_GetPropertyType
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPropertyDescription::GetPropertyType
 - propsys/IPropertyDescription::GetPropertyType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.h
api_name:
 - IPropertyDescription.GetPropertyType
---

# IPropertyDescription::GetPropertyType


## -description

Gets the variant type of the property.

## -parameters

### -param pvartype [out]

Type: <b><a href="/previous-versions/windows/desktop/legacy/ms221127(v=vs.85)">VARTYPE</a>*</b>

When this method returns, contains a pointer to a <a href="/previous-versions/windows/desktop/legacy/ms221127(v=vs.85)">VARTYPE</a> that indicates the property type. If the property is multi-valued, the value pointed to is a <b>VT_VECTOR</b> mask (<b>VT_VECTOR</b> ORed to the <b>VARTYPE</b>. The following are the possible variant types.



#### VT_NULL

Value can be any type. No coercion is performed. If a type cannot be retrieved, this method retrieves a default value of VT_NULL.



#### VT_LPWSTR

String



#### VT_BOOL

Boolean



#### VT_UI1

Byte



#### VT_I2

16-bit signed integer



#### VT_UI2

16-bit unsigned integer



#### VT_I4

32-bit signed integer



#### VT_UI4

32-bit unsigned integer



#### VT_I8

64-bit signed integer



#### VT_UI8

64-bit unsigned integer



#### VT_R8

Double



#### VT_FILETIME


<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure



#### VT_CLSID

GUID



#### VT_BLOB

Unspecified binary data



#### VT_UNKNOWN

Object that implements <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>




#### VT_STREAM

Object that implements <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>

## -returns

Type: <b>HRESULT</b>

This method always returns <b>S_OK</b>.

## -remarks

The information retrieved by this method comes from the <i>type</i> attribute of the <a href="/windows/desktop/properties/propdesc-schema-typeinfo">typeInfo</a> element in the property's .propdesc file.

## -see-also

<a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescription">IPropertyDescription</a>



<a href="/windows/desktop/properties/propdesc-schema-entry">Property Description Schema</a>
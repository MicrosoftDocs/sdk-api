---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IPropertyDescription::GetPropertyType


## -description


Gets the variant type of the property.


## -parameters




### -param pvartype [out]

Type: <b><a href="317b911b-1805-402d-a9cb-159546bc88b4">VARTYPE</a>*</b>

When this method returns, contains a pointer to a <a href="317b911b-1805-402d-a9cb-159546bc88b4">VARTYPE</a> that indicates the property type. If the property is multi-valued, the value pointed to is a <b>VT_VECTOR</b> mask (<b>VT_VECTOR</b> ORed to the <b>VARTYPE</b>. The following are the possible variant types.



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


<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure



#### VT_CLSID

GUID



#### VT_BLOB

Unspecified binary data



#### VT_UNKNOWN

Object that implements <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>




#### VT_STREAM

Object that implements <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>



## -returns



Type: <b>HRESULT</b>

This method always returns <b>S_OK</b>.




## -remarks



The information retrieved by this method comes from the <i>type</i> attribute of the <a href="shell.propdesc_schema_typeInfo">typeInfo</a> element in the property's .propdesc file.




## -see-also




<a href="shell.IPropertyDescription">IPropertyDescription</a>



<a href="https://msdn.microsoft.com/cac93c31-d90d-4116-b846-0cf593d1d56e">Property Description Schema</a>
 

 


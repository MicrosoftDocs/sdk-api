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

# VARENUM enumeration


## -description


Specifies the variant types.


## -enum-fields




### -field VT_EMPTY

Not specified.


### -field VT_NULL

Null.


### -field VT_I2

A 2-byte integer.


### -field VT_I4

A 4-byte integer.


### -field VT_R4

A 4-byte real.


### -field VT_R8

An 8-byte real.


### -field VT_CY

 Currency.


### -field VT_DATE

A date.


### -field VT_BSTR

A string.


### -field VT_DISPATCH

An <a href="https://msdn.microsoft.com/ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> pointer.


### -field VT_ERROR

An SCODE value.


### -field VT_BOOL

A Boolean value. True is -1 and false is 0.


### -field VT_VARIANT

A variant pointer.


### -field VT_UNKNOWN

An <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> pointer.


### -field VT_DECIMAL

A 16-byte fixed-pointer value.


### -field VT_I1

A character.


### -field VT_UI1

An unsigned character.


### -field VT_UI2

An unsigned short.


### -field VT_UI4

An unsigned long.


### -field VT_I8

A 64-bit integer.


### -field VT_UI8

A 64-bit unsigned integer.


### -field VT_INT

An integer.


### -field VT_UINT

An unsigned integer.


### -field VT_VOID

A C-style void.


### -field VT_HRESULT

An HRESULT value.


### -field VT_PTR

A pointer type.


### -field VT_SAFEARRAY

A safe array. Use VT_ARRAY in VARIANT.


### -field VT_CARRAY

A C-style array.


### -field VT_USERDEFINED

A user-defined type.


### -field VT_LPSTR

A null-terminated string.


### -field VT_LPWSTR

A wide null-terminated string.


### -field VT_RECORD

A user-defined type.


### -field VT_INT_PTR

A signed machine register size width.


### -field VT_UINT_PTR

An unsigned machine register size width.


### -field VT_FILETIME

A <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> value.


### -field VT_BLOB

Length-prefixed bytes.


### -field VT_STREAM

The name of the stream follows.


### -field VT_STORAGE

The name of the storage follows.


### -field VT_STREAMED_OBJECT

The stream contains an object.


### -field VT_STORED_OBJECT

The storage contains an object.


### -field VT_BLOB_OBJECT

The blob contains an object.


### -field VT_CF

A clipboard format.


### -field VT_CLSID

A class ID.


### -field VT_VERSIONED_STREAM

A stream with a GUID version.


### -field VT_BSTR_BLOB

Reserved.


### -field VT_VECTOR

A simple counted array.


### -field VT_ARRAY

A SAFEARRAY pointer.


### -field VT_BYREF

A void pointer for local use.


### -field VT_RESERVED


### -field VT_ILLEGAL


### -field VT_ILLEGALMASKED


### -field VT_TYPEMASK




## -remarks



The following table shows where these values can be used.

<table>
<tr>
<th>Value</th>
<th>VARIANT</th>
<th>TYPEDESC</th>
<th>Property set</th>
<th>Safe array</th>
</tr>
<tr>
<td><b>VT_ARRAY</b></td>
<td>X</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td><b>VT_BLOB</b></td>
<td></td>
<td></td>
<td>X</td>
<td></td>
</tr>
<tr>
<td><b>VT_BLOB_OBJECT</b></td>
<td></td>
<td></td>
<td>X</td>
<td></td>
</tr>
<tr>
<td><b>VT_BOOL</b></td>
<td>X</td>
<td>X</td>
<td>X</td>
<td>X</td>
</tr>
<tr>
<td><b>VT_BSTR</b></td>
<td>X</td>
<td>X</td>
<td>X</td>
<td>X</td>
</tr>
<tr>
<td><b>VT_BSTR_BLOB</b></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td><b>VT_BYREF</b></td>
<td>X</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td><b>VT_CARRAY</b></td>
<td></td>
<td>X</td>
<td></td>
<td></td>
</tr>
<tr>
<td><b>VT_CF</b></td>
<td></td>
<td></td>
<td>X</td>
<td></td>
</tr>
<tr>
<td><b>VT_CLSID</b></td>
<td></td>
<td></td>
<td>X</td>
<td></td>
</tr>
<tr>
<td><b>VT_CY</b></td>
<td>X</td>
<td>X</td>
<td>X</td>
<td>X</td>
</tr>
<tr>
<td><b>VT_DATE</b></td>
<td>X</td>
<td>X</td>
<td>X</td>
<td>X</td>
</tr>
<tr>
<td><b>VT_DECIMAL</b></td>
<td>X</td>
<td>X</td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>VT_DISPATCH</b></td>
<td>X</td>
<td>X</td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>VT_EMPTY</b></td>
<td>X</td>
<td></td>
<td>X</td>
<td></td>
</tr>
<tr>
<td><b>VT_ERROR</b></td>
<td>X</td>
<td>X</td>
<td>X</td>
<td>X</td>
</tr>
<tr>
<td><b>VT_FILETIME</b></td>
<td></td>
<td></td>
<td>X</td>
<td></td>
</tr>
<tr>
<td><b>VT_HRESULT</b></td>
<td></td>
<td></td>
<td>X</td>
<td></td>
</tr>
<tr>
<td><b>VT_I1</b></td>
<td>X</td>
<td>X</td>
<td>X</td>
<td>X</td>
</tr>
<tr>
<td><b>VT_I2</b></td>
<td>X</td>
<td>X</td>
<td>X</td>
<td>X</td>
</tr>
<tr>
<td><b>VT_I4</b></td>
<td>X</td>
<td>X</td>
<td>X</td>
<td>X</td>
</tr>
<tr>
<td><b>VT_I8</b></td>
<td></td>
<td>X</td>
<td>X</td>
<td></td>
</tr>
<tr>
<td><b>VT_INT</b></td>
<td>X</td>
<td>X</td>
<td>X</td>
<td>X</td>
</tr>
<tr>
<td><b>VT_INT_PTR</b></td>
<td></td>
<td></td>
<td>X</td>
<td></td>
</tr>
<tr>
<td><b>VT_LPSTR</b></td>
<td></td>
<td>X</td>
<td>X</td>
<td></td>
</tr>
<tr>
<td><b>VT_LPWSTR</b></td>
<td></td>
<td>X</td>
<td>X</td>
<td></td>
</tr>
<tr>
<td><b>VT_NULL</b></td>
<td>X</td>
<td></td>
<td>X</td>
<td></td>
</tr>
<tr>
<td><b>VT_PTR</b></td>
<td></td>
<td></td>
<td>X</td>
<td></td>
</tr>
<tr>
<td><b>VT_R4</b></td>
<td>X</td>
<td>X</td>
<td>X</td>
<td>X</td>
</tr>
<tr>
<td><b>VT_R8</b></td>
<td>X</td>
<td>X</td>
<td>X</td>
<td>X</td>
</tr>
<tr>
<td><b>VT_RECORD</b></td>
<td>X</td>
<td></td>
<td>X</td>
<td>X</td>
</tr>
<tr>
<td><b>VT_SAFEARRAY</b></td>
<td></td>
<td>X</td>
<td></td>
<td></td>
</tr>
<tr>
<td><b>VT_STORAGE</b></td>
<td></td>
<td></td>
<td>X</td>
<td></td>
</tr>
<tr>
<td><b>VT_STORED_OBJECT</b></td>
<td></td>
<td></td>
<td>X</td>
<td></td>
</tr>
<tr>
<td><b>VT_STREAM</b></td>
<td></td>
<td></td>
<td>X</td>
<td></td>
</tr>
<tr>
<td><b>VT_STREAMED_OBJECT</b></td>
<td></td>
<td></td>
<td>X</td>
<td></td>
</tr>
<tr>
<td><b>VT_UI1</b></td>
<td>X</td>
<td>X</td>
<td>X</td>
<td>X</td>
</tr>
<tr>
<td><b>VT_UI2</b></td>
<td>X</td>
<td>X</td>
<td>X</td>
<td>X</td>
</tr>
<tr>
<td><b>VT_UI4</b></td>
<td>X</td>
<td>X</td>
<td>X</td>
<td>X</td>
</tr>
<tr>
<td><b>VT_UI8</b></td>
<td></td>
<td>X</td>
<td>X</td>
<td></td>
</tr>
<tr>
<td><b>VT_UINT</b></td>
<td>X</td>
<td>X</td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>VT_UINT_PTR</b></td>
<td></td>
<td></td>
<td>X</td>
<td></td>
</tr>
<tr>
<td><b>VT_UNKNOWN</b></td>
<td>X</td>
<td>X</td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>VT_USERDEFINED</b></td>
<td></td>
<td></td>
<td>X</td>
<td></td>
</tr>
<tr>
<td><b>VT_VARIANT</b></td>
<td>X</td>
<td>X</td>
<td>X</td>
<td>X</td>
</tr>
<tr>
<td><b>VT_VECTOR</b></td>
<td></td>
<td></td>
<td>X</td>
<td></td>
</tr>
<tr>
<td><b>VT_VERSIONED_STREAM</b></td>
<td></td>
<td></td>
<td>X</td>
<td></td>
</tr>
<tr>
<td><b>VT_VOID</b></td>
<td></td>
<td></td>
<td>X</td>
<td></td>
</tr>
</table>
 

<b>VT_BSTR_BLOB</b> is reserved for system use.




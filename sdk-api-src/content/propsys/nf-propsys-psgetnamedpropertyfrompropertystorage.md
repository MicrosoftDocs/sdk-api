---
UID: NF:propsys.PSGetNamedPropertyFromPropertyStorage
title: PSGetNamedPropertyFromPropertyStorage function (propsys.h)
description: Gets a value from serialized property storage by property name.
helpviewer_keywords: ["PSGetNamedPropertyFromPropertyStorage","PSGetNamedPropertyFromPropertyStorage function [Windows Properties]","_shell_PSGetNamedPropertyFromPropertyStorage","properties.PSGetNamedPropertyFromPropertyStorage","propsys/PSGetNamedPropertyFromPropertyStorage","shell.PSGetNamedPropertyFromPropertyStorage"]
old-location: properties\PSGetNamedPropertyFromPropertyStorage.htm
tech.root: properties
ms.assetid: bb4eedc0-9ef5-46f2-83e5-340b77b3d876
ms.date: 12/05/2018
ms.keywords: PSGetNamedPropertyFromPropertyStorage, PSGetNamedPropertyFromPropertyStorage function [Windows Properties], _shell_PSGetNamedPropertyFromPropertyStorage, properties.PSGetNamedPropertyFromPropertyStorage, propsys/PSGetNamedPropertyFromPropertyStorage, shell.PSGetNamedPropertyFromPropertyStorage
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - PSGetNamedPropertyFromPropertyStorage
 - propsys/PSGetNamedPropertyFromPropertyStorage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - PSGetNamedPropertyFromPropertyStorage
---

# PSGetNamedPropertyFromPropertyStorage function


## -description

Gets a value from serialized property storage by property name.

## -parameters

### -param psps [in]

Type: <b>PCUSERIALIZEDPROPSTORAGE</b>

A pointer to an allocated buffer that contains the serialized properties. Call <a href="/windows/desktop/api/propsys/nf-propsys-ipersistserializedpropstorage-getpropertystorage">IPersistSerializedPropStorage::GetPropertyStorage</a> to obtain the buffer.

### -param cb [in]

Type: <b>DWORD</b>

The size, in bytes, of the USERIALIZESPROPSTORAGE buffer pointed to by <i>psps</i>.

### -param pszName [in]

Type: <b>LPCWSTR</b>

A pointer to a null-terminated, Unicode string that contains the name of the property.

### -param ppropvar [out]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

When this function returns, contains the requested value.

## -returns

Type: <b>PSSTDAPI</b>

Returns <b>S_OK</b> if successful, or an error value otherwise.

## -remarks

This function is intended to be called if the calling application already has a serialized property storage and needs no more than a few properties from storage. If many properties need to be retrieved, performance can be enhanced by creating a memory property store by calling <a href="/windows/desktop/api/propsys/nf-propsys-pscreatememorypropertystore">PSCreateMemoryPropertyStore</a>, initializing the property store by calling <a href="/windows/desktop/api/propsys/nf-propsys-ipersistserializedpropstorage-setpropertystorage">IPersistSerializedPropStorage::SetPropertyStorage</a>, and using <a href="/windows/desktop/api/propsys/nn-propsys-inamedpropertystore">INamedPropertyStore</a> or <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> to retrieve the properties.

Note that <a href="/windows/desktop/api/propsys/nf-propsys-psgetnamedpropertyfrompropertystorage">PSGetNamedPropertyFromPropertyStorage</a> works only on serialized buffers created by the system implementation of <a href="/windows/desktop/api/propsys/nn-propsys-ipersistserializedpropstorage">IPersistSerializedPropStorage</a>. You must first obtain a memory property store by calling <a href="/windows/desktop/api/propsys/nf-propsys-pscreatememorypropertystore">PSCreateMemoryPropertyStore</a>; that store can then create a serialized buffer using the <b>IPersistSerializedPropStorage</b> interface.

Although SERIALIZEDPROPSTORAGE is an opaque serialized data structure whose format may change in the future, earlier formats will be supported on subsequent versions of Windows. Because the format is opaque, applications should use supported property storage APIs to access and manipulate the serialized buffer (see <a href="/windows/desktop/api/propsys/nn-propsys-ipersistserializedpropstorage">IPersistSerializedPropStorage</a> and  <a href="/windows/desktop/api/propsys/nf-propsys-psgetpropertyfrompropertystorage">PSGetPropertyFromPropertyStorage</a>).


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propsys/nf-propsys-psgetnamedpropertyfrompropertystorage">PSGetNamedPropertyFromPropertyStorage</a> to read a value from serialized property storage.


```cpp
// SERIALIZEDPROPSTORAGE *pStorage;
// DWORD cbStorage;
// Assume the variables pStorage and cbStorage are initialized and valid.  
PROPVARIANT propvar;

HRESULT hr = PSGetNamedPropertyFromPropertyStorage(pStorage, cb, L"MyProperty", &propvar);

if (SUCCEEDED(hr))
{
    // propvar is now valid.
 
    PropVariantClear(&propvar);
}
```

## -see-also

<a href="/windows/desktop/api/propsys/nf-propsys-psgetpropertyfrompropertystorage">PSGetPropertyFromPropertyStorage</a>
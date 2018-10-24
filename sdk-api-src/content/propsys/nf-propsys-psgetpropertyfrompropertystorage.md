---
UID: NF:propsys.PSGetPropertyFromPropertyStorage
title: PSGetPropertyFromPropertyStorage function
author: windows-sdk-content
description: Gets the value of a property as stored in serialized property storage.
old-location: properties\PSGetPropertyFromPropertyStorage.htm
tech.root: properties
ms.assetid: c649d25d-7971-4804-a5a2-3fd6860659b4
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: PSGetPropertyFromPropertyStorage, PSGetPropertyFromPropertyStorage function [Windows Properties], _shell_PSGetPropertyFromPropertyStorage, properties.PSGetPropertyFromPropertyStorage, propsys/PSGetPropertyFromPropertyStorage, shell.PSGetPropertyFromPropertyStorage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - PSGetPropertyFromPropertyStorage
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# PSGetPropertyFromPropertyStorage function


## -description


Gets the value of a property as stored in serialized property storage.


## -parameters




### -param psps [in]

Type: <b>PCUSERIALIZEDPROPSTORAGE</b>

Pointer to an allocated buffer that contains the serialized properties. This buffer is obtained by a call to <a href="https://msdn.microsoft.com/86a1d7ec-759a-4b8a-91e1-4cfa28a17b41">IPersistSerializedPropStorage::GetPropertyStorage</a>.


### -param cb [in]

Type: <b>DWORD</b>

The size, in bytes, of the <b>USERIALIZESPROPSTORAGE</b> buffer pointed to by <i>psps</i>.


### -param rpkey [in]

Type: <b>REFPROPERTYKEY</b>

Reference to the <a href="https://msdn.microsoft.com/en-us/library/Bb773381(v=VS.85).aspx">PROPERTYKEY</a> that identifies the property for which to get the value.


### -param ppropvar [out]

Type: <b><a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>**</b>

When this function returns, contains the requested value.


## -returns



Type: <b>PSSTDAPI</b>

Returns <b>S_OK</b> if successful, or an error value otherwise.




## -remarks



This function is intended to be called if the calling application already has a serialized property storage and needs no more than a few properties from storage. If many properties need to be retrieved, performance can be enhanced by creating a memory property store through <a href="https://msdn.microsoft.com/en-us/library/Bb776489(v=VS.85).aspx">PSCreateMemoryPropertyStore</a>, initializing the property store by calling <a href="https://msdn.microsoft.com/5b6d14ba-3de3-493e-8551-0f3caa02f339">IPersistSerializedPropStorage::SetPropertyStorage</a>, and by using <a href="https://msdn.microsoft.com/en-us/library/Bb761474(v=VS.85).aspx">IPropertyStore</a> to retrieve the properties.

Note that <a href="https://msdn.microsoft.com/en-us/library/Bb762080(v=VS.85).aspx">PSGetPropertyFromPropertyStorage</a> works only on serialized buffers created by the system implementation of <a href="https://msdn.microsoft.com/d3ce6a05-b1e5-4d99-a27e-3a97a28ed8e8">IPersistSerializedPropStorage</a>. You must first obtain a memory property store by calling <a href="https://msdn.microsoft.com/en-us/library/Bb776489(v=VS.85).aspx">PSCreateMemoryPropertyStore</a>. That store can then create a serialized buffer using the <b>IPersistSerializedPropStorage</b> interface.

Although SERIALIZEDPROPSTORAGE is an opaque serialized data structure whose format may change in the future, earlier formats will be supported on subsequent versions of Windows. Because the format is opaque, applications should use supported property storage APIs to access and manipulate the serialized buffer (see <a href="https://msdn.microsoft.com/d3ce6a05-b1e5-4d99-a27e-3a97a28ed8e8">IPersistSerializedPropStorage</a>).


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="https://msdn.microsoft.com/en-us/library/Bb762080(v=VS.85).aspx">PSGetPropertyFromPropertyStorage</a> to read a value from serialized property storage.


```cpp
// SERIALIZEDPROPSTORAGE *pStorage;
// DWORD cbStorage;
// Assume the variables pStorage and cbStorage are initialized and valid.  
PROPVARIANT propvar;

HRESULT hr = PSGetPropertyFromPropertyStorage(pStorage, cb, PKEY_Rating, &propvar);

if (SUCCEEDED(hr))
{
    // propvar is now valid.
 
    PropVariantClear(&propvar);
}
```





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb776501(v=VS.85).aspx">PSGetNamedPropertyFromPropertyStorage</a>
 

 


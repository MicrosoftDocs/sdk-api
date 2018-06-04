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

Reference to the <a href="shell.PROPERTYKEY">PROPERTYKEY</a> that identifies the property for which to get the value.


### -param ppropvar [out]

Type: <b><a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>**</b>

When this function returns, contains the requested value.


## -returns



Type: <b>PSSTDAPI</b>

Returns <b>S_OK</b> if successful, or an error value otherwise.




## -remarks



This function is intended to be called if the calling application already has a serialized property storage and needs no more than a few properties from storage. If many properties need to be retrieved, performance can be enhanced by creating a memory property store through <a href="shell.PSCreateMemoryPropertyStore">PSCreateMemoryPropertyStore</a>, initializing the property store by calling <a href="https://msdn.microsoft.com/5b6d14ba-3de3-493e-8551-0f3caa02f339">IPersistSerializedPropStorage::SetPropertyStorage</a>, and by using <a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a> to retrieve the properties.

Note that <a href="shell.PSGetPropertyFromPropertyStorage">PSGetPropertyFromPropertyStorage</a> works only on serialized buffers created by the system implementation of <a href="https://msdn.microsoft.com/d3ce6a05-b1e5-4d99-a27e-3a97a28ed8e8">IPersistSerializedPropStorage</a>. You must first obtain a memory property store by calling <a href="shell.PSCreateMemoryPropertyStore">PSCreateMemoryPropertyStore</a>. That store can then create a serialized buffer using the <b>IPersistSerializedPropStorage</b> interface.

Although SERIALIZEDPROPSTORAGE is an opaque serialized data structure whose format may change in the future, earlier formats will be supported on subsequent versions of Windows. Because the format is opaque, applications should use supported property storage APIs to access and manipulate the serialized buffer (see <a href="https://msdn.microsoft.com/d3ce6a05-b1e5-4d99-a27e-3a97a28ed8e8">IPersistSerializedPropStorage</a>).


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.PSGetPropertyFromPropertyStorage">PSGetPropertyFromPropertyStorage</a> to read a value from serialized property storage.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// SERIALIZEDPROPSTORAGE *pStorage;
// DWORD cbStorage;
// Assume the variables pStorage and cbStorage are initialized and valid.  
PROPVARIANT propvar;

HRESULT hr = PSGetPropertyFromPropertyStorage(pStorage, cb, PKEY_Rating, &amp;propvar);

if (SUCCEEDED(hr))
{
    // propvar is now valid.
 
    PropVariantClear(&amp;propvar);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.PSGetNamedPropertyFromPropertyStorage">PSGetNamedPropertyFromPropertyStorage</a>
 

 


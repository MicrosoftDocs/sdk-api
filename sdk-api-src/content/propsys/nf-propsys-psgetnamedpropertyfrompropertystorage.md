---
UID: NF:propsys.PSGetNamedPropertyFromPropertyStorage
title: PSGetNamedPropertyFromPropertyStorage function
author: windows-sdk-content
description: Gets a value from serialized property storage by property name.
old-location: properties\PSGetNamedPropertyFromPropertyStorage.htm
tech.root: properties
ms.assetid: bb4eedc0-9ef5-46f2-83e5-340b77b3d876
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PSGetNamedPropertyFromPropertyStorage, PSGetNamedPropertyFromPropertyStorage function [Windows Properties], _shell_PSGetNamedPropertyFromPropertyStorage, properties.PSGetNamedPropertyFromPropertyStorage, propsys/PSGetNamedPropertyFromPropertyStorage, shell.PSGetNamedPropertyFromPropertyStorage
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
 - PSGetNamedPropertyFromPropertyStorage
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# PSGetNamedPropertyFromPropertyStorage function


## -description


Gets a value from serialized property storage by property name.


## -parameters




### -param psps [in]

Type: <b>PCUSERIALIZEDPROPSTORAGE</b>

A pointer to an allocated buffer that contains the serialized properties. Call <a href="https://msdn.microsoft.com/86a1d7ec-759a-4b8a-91e1-4cfa28a17b41">IPersistSerializedPropStorage::GetPropertyStorage</a> to obtain the buffer.


### -param cb [in]

Type: <b>DWORD</b>

The size, in bytes, of the USERIALIZESPROPSTORAGE buffer pointed to by <i>psps</i>.


### -param pszName [in]

Type: <b>LPCWSTR</b>

A pointer to a null-terminated, Unicode string that contains the name of the property.


### -param ppropvar [out]

Type: <b><a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>*</b>

When this function returns, contains the requested value.


## -returns



Type: <b>PSSTDAPI</b>

Returns <b>S_OK</b> if successful, or an error value otherwise.




## -remarks



This function is intended to be called if the calling application already has a serialized property storage and needs no more than a few properties from storage. If many properties need to be retrieved, performance can be enhanced by creating a memory property store by calling <a href="shell.PSCreateMemoryPropertyStore">PSCreateMemoryPropertyStore</a>, initializing the property store by calling <a href="https://msdn.microsoft.com/5b6d14ba-3de3-493e-8551-0f3caa02f339">IPersistSerializedPropStorage::SetPropertyStorage</a>, and using <a href="https://msdn.microsoft.com/5f7997ba-a5c8-42b5-90c8-5cb34afd6092">INamedPropertyStore</a> or <a href="shell.IPropertyStore">IPropertyStore</a> to retrieve the properties.

Note that <a href="shell.PSGetNamedPropertyFromPropertyStorage">PSGetNamedPropertyFromPropertyStorage</a> works only on serialized buffers created by the system implementation of <a href="https://msdn.microsoft.com/d3ce6a05-b1e5-4d99-a27e-3a97a28ed8e8">IPersistSerializedPropStorage</a>. You must first obtain a memory property store by calling <a href="shell.PSCreateMemoryPropertyStore">PSCreateMemoryPropertyStore</a>; that store can then create a serialized buffer using the <b>IPersistSerializedPropStorage</b> interface.

Although SERIALIZEDPROPSTORAGE is an opaque serialized data structure whose format may change in the future, earlier formats will be supported on subsequent versions of Windows. Because the format is opaque, applications should use supported property storage APIs to access and manipulate the serialized buffer (see <a href="https://msdn.microsoft.com/d3ce6a05-b1e5-4d99-a27e-3a97a28ed8e8">IPersistSerializedPropStorage</a> and  <a href="shell.PSGetPropertyFromPropertyStorage">PSGetPropertyFromPropertyStorage</a>).


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.PSGetNamedPropertyFromPropertyStorage">PSGetNamedPropertyFromPropertyStorage</a> to read a value from serialized property storage.

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

HRESULT hr = PSGetNamedPropertyFromPropertyStorage(pStorage, cb, L"MyProperty", &amp;propvar);

if (SUCCEEDED(hr))
{
    // propvar is now valid.
 
    PropVariantClear(&amp;propvar);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.PSGetPropertyFromPropertyStorage">PSGetPropertyFromPropertyStorage</a>
 

 


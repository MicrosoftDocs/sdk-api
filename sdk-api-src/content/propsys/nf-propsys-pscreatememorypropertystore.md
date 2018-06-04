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

# PSCreateMemoryPropertyStore function


## -description


Creates an in-memory property store.


## -parameters




### -param riid [in]

Type: <b>REFIID</b>

Reference to the requested interface ID.


### -param ppv [out]

Type: <b>void**</b>

When this function returns, contains a pointer to the desired interface, typically <a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a> or <a href="https://msdn.microsoft.com/d3ce6a05-b1e5-4d99-a27e-3a97a28ed8e8">IPersistSerializedPropStorage</a>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function creates an in-memory property store object that implements <a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a>, <a href="https://msdn.microsoft.com/5f7997ba-a5c8-42b5-90c8-5cb34afd6092">INamedPropertyStore</a>, <a href="shell.IPropertyStoreCache">IPropertyStoreCache</a>, <a href="https://msdn.microsoft.com/97ea64ee-d950-4872-add6-1f532a6eb33f">IPersistStream</a>, <a href="_inet_IPropertyBag_Interface_cpp">IPropertyBag</a>, and <a href="https://msdn.microsoft.com/d3ce6a05-b1e5-4d99-a27e-3a97a28ed8e8">IPersistSerializedPropStorage</a>.

The memory property store does not correspond to a file and is designed for use as a cache. <a href="https://msdn.microsoft.com/library/windows/hardware/ff536957">IPropertyStore::Commit</a> is a no-op, and the data stored in the object persists only as long as the object does.

The memory property store is thread safe. It aggregates the free-threaded marshaller and uses critical sections to protect its data members.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.PSCreateMemoryPropertyStore">PSCreateMemoryPropertyStore</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>IPropertyStore *ppropstore;

HRESULT hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&amp;ppropstore));

if (SUCCEEDED(hr))
{
    // ppropstore is now valid.  
    ppropstore-&gt;Release();
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.PSCreateMultiplexPropertyStore">PSCreateMultiplexPropertyStore</a>
 

 


---
UID: NF:propsys.PSCreateMemoryPropertyStore
title: PSCreateMemoryPropertyStore function
author: windows-sdk-content
description: Creates an in-memory property store.
old-location: properties\PSCreateMemoryPropertyStore.htm
tech.root: properties
ms.assetid: 6e7a2ac0-2a4a-41ec-a2a8-ddbe8aa45bc9
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: PSCreateMemoryPropertyStore, PSCreateMemoryPropertyStore function [Windows Properties], _shell_PSCreateMemoryPropertyStore, properties.PSCreateMemoryPropertyStore, propsys/PSCreateMemoryPropertyStore, shell.PSCreateMemoryPropertyStore
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
 - Ext-MS-Win-shell-propsys-l1-1-0.dll
api_name:
 - PSCreateMemoryPropertyStore
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
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

When this function returns, contains a pointer to the desired interface, typically <a href="shell.IPropertyStore">IPropertyStore</a> or <a href="https://msdn.microsoft.com/d3ce6a05-b1e5-4d99-a27e-3a97a28ed8e8">IPersistSerializedPropStorage</a>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function creates an in-memory property store object that implements <a href="shell.IPropertyStore">IPropertyStore</a>, <a href="https://msdn.microsoft.com/5f7997ba-a5c8-42b5-90c8-5cb34afd6092">INamedPropertyStore</a>, <a href="shell.IPropertyStoreCache">IPropertyStoreCache</a>, <a href="https://msdn.microsoft.com/97ea64ee-d950-4872-add6-1f532a6eb33f">IPersistStream</a>, <a href="_inet_IPropertyBag_Interface_cpp">IPropertyBag</a>, and <a href="https://msdn.microsoft.com/d3ce6a05-b1e5-4d99-a27e-3a97a28ed8e8">IPersistSerializedPropStorage</a>.

The memory property store does not correspond to a file and is designed for use as a cache. <a href="shell.IPropertyStore_Commit">IPropertyStore::Commit</a> is a no-op, and the data stored in the object persists only as long as the object does.

The memory property store is thread safe. It aggregates the free-threaded marshaller and uses critical sections to protect its data members.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.PSCreateMemoryPropertyStore">PSCreateMemoryPropertyStore</a>.


```cpp
IPropertyStore *ppropstore;

HRESULT hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&ppropstore));

if (SUCCEEDED(hr))
{
    // ppropstore is now valid.  
    ppropstore->Release();
}
```





## -see-also




<a href="shell.PSCreateMultiplexPropertyStore">PSCreateMultiplexPropertyStore</a>
 

 


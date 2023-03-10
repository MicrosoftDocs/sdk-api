---
UID: NF:propsys.PSCreateMemoryPropertyStore
title: PSCreateMemoryPropertyStore function (propsys.h)
description: Creates an in-memory property store.
helpviewer_keywords: ["PSCreateMemoryPropertyStore","PSCreateMemoryPropertyStore function [Windows Properties]","_shell_PSCreateMemoryPropertyStore","properties.PSCreateMemoryPropertyStore","propsys/PSCreateMemoryPropertyStore","shell.PSCreateMemoryPropertyStore"]
old-location: properties\PSCreateMemoryPropertyStore.htm
tech.root: properties
ms.assetid: 6e7a2ac0-2a4a-41ec-a2a8-ddbe8aa45bc9
ms.date: 12/05/2018
ms.keywords: PSCreateMemoryPropertyStore, PSCreateMemoryPropertyStore function [Windows Properties], _shell_PSCreateMemoryPropertyStore, properties.PSCreateMemoryPropertyStore, propsys/PSCreateMemoryPropertyStore, shell.PSCreateMemoryPropertyStore
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
 - PSCreateMemoryPropertyStore
 - propsys/PSCreateMemoryPropertyStore
dev_langs:
 - c++
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

When this function returns, contains a pointer to the desired interface, typically <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> or <a href="/windows/desktop/api/propsys/nn-propsys-ipersistserializedpropstorage">IPersistSerializedPropStorage</a>.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function creates an in-memory property store object that implements <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a>, <a href="/windows/desktop/api/propsys/nn-propsys-inamedpropertystore">INamedPropertyStore</a>, <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystorecache">IPropertyStoreCache</a>, <a href="/windows/desktop/api/objidl/nn-objidl-ipersiststream">IPersistStream</a>, <a href="../oaidl/nn-oaidl-ipropertybag.md">IPropertyBag</a>, and <a href="/windows/desktop/api/propsys/nn-propsys-ipersistserializedpropstorage">IPersistSerializedPropStorage</a>.

The memory property store does not correspond to a file and is designed for use as a cache. <a href="/windows/desktop/api/propsys/nf-propsys-ipropertystore-commit">IPropertyStore::Commit</a> is a no-op, and the data stored in the object persists only as long as the object does.

The memory property store is thread safe. It aggregates the free-threaded marshaller and uses critical sections to protect its data members.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propsys/nf-propsys-pscreatememorypropertystore">PSCreateMemoryPropertyStore</a>.


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

<a href="/windows/desktop/api/propsys/nf-propsys-pscreatemultiplexpropertystore">PSCreateMultiplexPropertyStore</a>
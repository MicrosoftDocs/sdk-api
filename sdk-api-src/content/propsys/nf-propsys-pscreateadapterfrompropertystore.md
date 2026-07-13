---
UID: NF:propsys.PSCreateAdapterFromPropertyStore
title: PSCreateAdapterFromPropertyStore function (propsys.h)
description: Creates an adapter from an IPropertyStore.
helpviewer_keywords: ["PSCreateAdapterFromPropertyStore","PSCreateAdapterFromPropertyStore function [Windows Properties]","_shell_PSCreateAdapterFromPropertyStore","properties.PSCreateAdapterFromPropertyStore","propsys/PSCreateAdapterFromPropertyStore","shell.PSCreateAdapterFromPropertyStore"]
old-location: properties\PSCreateAdapterFromPropertyStore.htm
tech.root: properties
ms.assetid: a3489f95-e790-481a-af6e-f30527dc476c
ms.date: 12/05/2018
ms.keywords: PSCreateAdapterFromPropertyStore, PSCreateAdapterFromPropertyStore function [Windows Properties], _shell_PSCreateAdapterFromPropertyStore, properties.PSCreateAdapterFromPropertyStore, propsys/PSCreateAdapterFromPropertyStore, shell.PSCreateAdapterFromPropertyStore
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
 - PSCreateAdapterFromPropertyStore
 - propsys/PSCreateAdapterFromPropertyStore
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-propsys-l1-1-1.dll
 - Propsys.dll
 - Ext-MS-Win-shell-propsys-l1-1-0.dll
api_name:
 - PSCreateAdapterFromPropertyStore
---

# PSCreateAdapterFromPropertyStore function


## -description

Creates an adapter from an <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a>.

## -parameters

### -param pps [in]

Type: <b><a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a>*</b>

Pointer to an <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> object that represents the property store.

### -param riid [in]

Type: <b>REFIID</b>

Reference to an IID.

### -param ppv [out]

Type: <b>void**</b>

When this function returns, contains the interface pointer requested in <i>riid</i>.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The adapter object implements <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage">IPropertySetStorage</a>, <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a>, <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystorecapabilities">IPropertyStoreCapabilities</a>, and <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectprovider">IObjectProvider</a>.

Use this function if you need an object that implements <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> with an API that requires an <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage">IPropertySetStorage</a> interface. The object created can also be useful to a namespace extension that wants to provide support for binding to namespace items using <b>IPropertySetStorage</b>. Applications must call this object from only one thread at a time.

The adapter property store created by this function retains a reference to the source <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> interface. Therefore, the calling application is free to release its reference to the source <b>IPropertyStore</b> whenever convenient after calling this function.

The adapter property store makes calls to methods on the <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> interface as appropriate. Therefore, if the calling application is writing values to the store, it should call the <a href="/windows/desktop/api/propsys/nf-propsys-ipropertystore-commit">IPropertyStore::Commit</a> method on only one of the interfaces.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propsys/nf-propsys-pscreateadapterfrompropertystore">PSCreateAdapterFromPropertyStore</a> to use an adapter property store to convert an <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> interface into an <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage">IPropertySetStorage</a> interface.


```cpp
// IPropertyStore *ppropstore;
// Assume variable ppropstore is initialized and valid
IPropertySetStorage *pSetStorage;

HRESULT hr = PSCreateadapterFromPropertyStore(ppropstore, IID_PPV_ARGS(&pSetStorage));

if (SUCCEEDED(hr))
{
    // pSetStorage is now valid and can be used to access the data in ppropstore.
    pSetStorage->Release();
}
```

## -see-also

<a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage">IPropertySetStorage</a>



<a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a>



<a href="/windows/desktop/api/propsys/nf-propsys-pscreatepropertystorefrompropertysetstorage">PSCreatePropertyStoreFromPropertySetStorage</a>
---
UID: NF:propsys.PSCreateDelayedMultiplexPropertyStore
title: PSCreateDelayedMultiplexPropertyStore function (propsys.h)
description: Creates a read-only, delayed-binding property store that contains multiple property stores.
helpviewer_keywords: ["PSCreateDelayedMultiplexPropertyStore","PSCreateDelayedMultiplexPropertyStore function [Windows Properties]","_shell_PSCreateDelayedMultiplexPropertyStore","properties.PSCreateDelayedMultiplexPropertyStore","propsys/PSCreateDelayedMultiplexPropertyStore","shell.PSCreateDelayedMultiplexPropertyStore"]
old-location: properties\PSCreateDelayedMultiplexPropertyStore.htm
tech.root: properties
ms.assetid: 8b264d7e-6124-4724-8d23-605101705893
ms.date: 12/05/2018
ms.keywords: PSCreateDelayedMultiplexPropertyStore, PSCreateDelayedMultiplexPropertyStore function [Windows Properties], _shell_PSCreateDelayedMultiplexPropertyStore, properties.PSCreateDelayedMultiplexPropertyStore, propsys/PSCreateDelayedMultiplexPropertyStore, shell.PSCreateDelayedMultiplexPropertyStore
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
 - PSCreateDelayedMultiplexPropertyStore
 - propsys/PSCreateDelayedMultiplexPropertyStore
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
 - PSCreateDelayedMultiplexPropertyStore
---

# PSCreateDelayedMultiplexPropertyStore function


## -description

Creates a read-only, delayed-binding property store that contains multiple property stores.

## -parameters

### -param flags

Type: <b><a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags">GETPROPERTYSTOREFLAGS</a></b>

One or more <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags">GETPROPERTYSTOREFLAGS</a> values. These values specify details of the created property store object.

### -param pdpsf

Type: <b><a href="/windows/desktop/api/propsys/nn-propsys-idelayedpropertystorefactory">IDelayedPropertyStoreFactory</a>*</b>

Interface pointer to an instance of <a href="/windows/desktop/api/propsys/nn-propsys-idelayedpropertystorefactory">IDelayedPropertyStoreFactory</a>.

### -param rgStoreIds [in]

Type: <b>const DWORD*</b>

Pointer to an array of property store IDs. This array does not need to be initialized.

### -param cStores [in]

Type: <b>DWORD</b>

The number of elements in the array pointed to by <i>rgStoreIds</i>.

### -param riid [in]

Type: <b>REFIID</b>

Reference to the requested IID of the interface that will represent the created property store.

### -param ppv [out]

Type: <b>void**</b>

When this function returns, contains the interface pointer requested in <i>riid</i>. This is typically <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a>.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function creates a Component Object Model (COM) object that implements <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a>, 
 <a href="/windows/desktop/api/propsys/nn-propsys-inamedpropertystore">INamedPropertyStore</a>, <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectprovider">IObjectProvider</a>, and <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystorecapabilities">IPropertyStoreCapabilities</a>.

Applications must call this object from only one thread at a time.

You must initialize COM with <a href="/windows/desktop/api/objbase/nf-objbase-coinitialize">CoInitialize</a> or <a href="/windows/desktop/api/ole2/nf-ole2-oleinitialize">OleInitialize</a> before you call <a href="/windows/desktop/api/propsys/nf-propsys-pscreatedelayedmultiplexpropertystore">PSCreateDelayedMultiplexPropertyStore</a>. COM must remain initialized for the lifetime of this object.


<a href="/windows/desktop/api/propsys/nf-propsys-pscreatedelayedmultiplexpropertystore">PSCreateDelayedMultiplexPropertyStore</a> is designed as an alternative to <a href="/windows/desktop/api/propsys/nf-propsys-pscreatemultiplexpropertystore">PSCreateMultiplexPropertyStore</a>, which requires that the array of property stores be initialized before it creates the multiplex property store.

The delayed binding mechanism is designed as a performance enhancement for calls to <a href="/windows/desktop/api/propsys/nf-propsys-ipropertystore-getvalue">IPropertyStore::GetValue</a> on a multiplex property store. When asked for the value of a property, the delayed multiplex property store checks each of the property stores for the value. After the value is found, there is no need to create and initialize subsequent stores. The delayed multiplex property store stops searching for a value when one of the property stores returns a success code and a non-VT_EMPTY value.

When the delayed multiplex property store needs to access a particular property store, it first checks to see if it has already obtained an interface to that property store. If not, it calls <a href="/windows/desktop/api/propsys/nf-propsys-idelayedpropertystorefactory-getdelayedpropertystore">IDelayedPropertyStoreFactory::GetDelayedPropertyStore</a> with the appropriate property store ID to obtain the property store. It always uses the property store IDs in the order in which they are provided by the application. It is possible that not all IDs will be used.

If the call to <a href="/windows/desktop/api/propsys/nn-propsys-idelayedpropertystorefactory">IDelayedPropertyStoreFactory</a> fails with E_NOTIMPL or E_ACCESSDENIED for a particular property store ID, or if the application specified <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags">GPS_BESTEFFORT</a>, then the failure is ignored and the delayed multiplex property store moves on to the next property store.

In some cases, it might be beneficial to use <a href="/windows/desktop/api/propsys/nf-propsys-pscreatedelayedmultiplexpropertystore">PSCreateDelayedMultiplexPropertyStore</a> in place of <a href="/windows/desktop/api/propsys/nf-propsys-pscreatemultiplexpropertystore">PSCreateMultiplexPropertyStore</a>. For example, if an application needs to multiplex two property stores and the first property store is not memory-intensive to initialize and provides PKEY_Size information. Often, calling applications ask for a multiplex property store and then ask for only PKEY_Size before they release the object. In such a case, the application could avoid the cost of initializing the second property store by calling <b>PSCreateDelayedMultiplexPropertyStore</b> and implementing <a href="/windows/desktop/api/propsys/nn-propsys-idelayedpropertystorefactory">IDelayedPropertyStoreFactory</a>.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propsys/nf-propsys-pscreatedelayedmultiplexpropertystore">PSCreateDelayedMultiplexPropertyStore</a> in an implementation of <a href="/windows/desktop/api/propsys/nf-propsys-ipropertystorefactory-getpropertystore">IPropertyStoreFactory::GetPropertyStore</a>.


```cpp
// CMyFactory is a reference-counted COM object that implements both IPropertyStoreFactory and IDelayedPropertyStoreFactory.

// CMyFactory is assumed to be fully implemented, but for the sake of brevity, 
// many functions are not shown here. 

// Private functions are indicated with an underscore prefix.

// The hope is that the fastest property store satisfies the caller's queries 
// so that the slower property stores are never created.
 
// CMyFactory implementation for IPropertyStoreFactory::GetPropertyStore
HRESULT CMyFactory::GetPropertyStore( __in GETPROPERTYSTOREFLAGS flags,
                                      __in_opt IUnknown *pUnkFactory,
                                      __in REFIID riid,
                                      __deref_out void **ppv)
{
    *ppv = NULL;
    HRESULT hr;
 
    // This application creates only read-only stores.
    if (flags & GPS_READWRITE)
    {
        hr = STG_E_ACCESSDENIED;
    }
    else
    {
        // More advanced applications would check other GETPROPERTYSTOREFLAGS 
        // flags and respond appropriately.
 
        // This application always creates its stores in-process, so it 
        // ignores the pUnkFactory value.
        
        DWORD rgStoreIds[] = {0, 1, 2};
        
        hr = PSCreateDelayedMultiplexPropertyStore(flags, this, rgStoreIds, ARRAYSIZE(rgStoreIds), riid, ppv);
    }
 
    return hr;
}
 
// CMyFactory implementation of IDelayedPropertyStoreFactory::GetDelayedPropertyStore
HRESULT CMyFactory::GetDelayedPropertyStore(GETPROPERTYSTOREFLAGS flags,
                                            DWORD dwStoreId,
                                            REFIID riid,
                                            void **ppv)
{
    *ppv = NULL;
    HRESULT hr;
    
    // Note: The IDs here match the IDs in rgStoreIds above.

    if (dwStoreId == 0)
    {
        // This store is the fastest at returning properties.

        hr = _CreateFastestPropertyStore(flags, riid, ppv);
    }
    else if (dwStoreId == 1)
    {
        // This store is slower at returning properties.
        hr = _CreateSlowerPropertyStore(flags, riid, ppv);
    }
    else if (dwStoreId == 2)
    {
        // This store is very slow at returning properties.
        hr = _CreateSlowestPropertyStore(flags, riid, ppv);
    }
    else
    {
        // This should never happen.
        hr = E_UNEXPECTED;
    }
    
    return hr;
}
```

## -see-also

<a href="/windows/desktop/api/propsys/nn-propsys-ipropertystorefactory">IPropertyStoreFactory</a>



<a href="/windows/desktop/api/propsys/nf-propsys-pscreatemultiplexpropertystore">PSCreateMultiplexPropertyStore</a>
---
UID: NF:propsys.PSCreateMultiplexPropertyStore
title: PSCreateMultiplexPropertyStore function (propsys.h)
author: windows-sdk-content
description: Creates a read-only property store that contains multiple property stores, each of which must support either IPropertyStore or IPropertySetStorage.
old-location: properties\PSCreateMultiplexPropertyStore.htm
tech.root: properties
ms.assetid: 4a6b5a10-5ef2-42c7-bf3b-dfa743be252f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PSCreateMultiplexPropertyStore, PSCreateMultiplexPropertyStore function [Windows Properties], _shell_PSCreateMultiplexPropertyStore, properties.PSCreateMultiplexPropertyStore, propsys/PSCreateMultiplexPropertyStore, shell.PSCreateMultiplexPropertyStore
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
 - PSCreateMultiplexPropertyStore
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# PSCreateMultiplexPropertyStore function


## -description


Creates a read-only property store that contains multiple property stores, each of which must support either <a href="https://msdn.microsoft.com/en-us/library/Bb761474(v=VS.85).aspx">IPropertyStore</a> or <a href="https://msdn.microsoft.com/0ea3e1e0-c135-4138-81e4-f72412fc3128">IPropertySetStorage</a>.


## -parameters




### -param prgpunkStores [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>**</b>

Address of a pointer to an array of property stores that implement either <a href="https://msdn.microsoft.com/en-us/library/Bb761474(v=VS.85).aspx">IPropertyStore</a> or <a href="https://msdn.microsoft.com/0ea3e1e0-c135-4138-81e4-f72412fc3128">IPropertySetStorage</a>.


### -param cStores [in]

Type: <b>DWORD</b>

The number of elements in the array referenced in <i>prgpunkStores</i>.


### -param riid [in]

Type: <b>REFIID</b>

Reference to the requested IID.


### -param ppv [out]

Type: <b>void**</b>

When this function returns, contains the interface pointer requested in <i>riid</i>. This is typically <a href="https://msdn.microsoft.com/en-us/library/Bb761474(v=VS.85).aspx">IPropertyStore</a>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function creates a Component Object Model (COM) object that implements <a href="https://msdn.microsoft.com/en-us/library/Bb761474(v=VS.85).aspx">IPropertyStore</a>, <a href="https://msdn.microsoft.com/5f7997ba-a5c8-42b5-90c8-5cb34afd6092">INamedPropertyStore</a>, <a href="https://msdn.microsoft.com/477991e5-0882-475c-9178-c3add695dc2c">IObjectProvider</a>, and <a href="https://msdn.microsoft.com/en-us/library/Bb761452(v=VS.85).aspx">IPropertyStoreCapabilities</a>. The multiplex property store object aggregates the properties exposed from multiple property stores.

This object can be useful for aggregating the properties from multiple existing property store implementations in a Shell namespace extension, or for reusing an existing property store and providing additional read-only properties.

Applications must call this object from only one thread at a time.

You must initialize COM with <a href="https://msdn.microsoft.com/0f171cf4-87b9-43a6-97f2-80ed344fe376">CoInitialize</a> or <a href="https://msdn.microsoft.com/9a13e7a0-f2e2-466b-98f5-38d5972fa391">OleInitialize</a> before you call <a href="https://msdn.microsoft.com/en-us/library/Bb776488(v=VS.85).aspx">PSCreateDelayedMultiplexPropertyStore</a>. COM must remain initialized for the lifetime of this object.

Each of the objects in the array <i>prgpunkStores</i> must implement either <a href="https://msdn.microsoft.com/en-us/library/Bb761474(v=VS.85).aspx">IPropertyStore</a> or <a href="https://msdn.microsoft.com/0ea3e1e0-c135-4138-81e4-f72412fc3128">IPropertySetStorage</a>. If an object implements <b>IPropertySetStorage</b>, it is wrapped using <a href="https://msdn.microsoft.com/en-us/library/Bb776493(v=VS.85).aspx">PSCreatePropertyStoreFromPropertySetStorage</a> for use in the multiplex property store.

The multiplex property store implementation of <a href="https://msdn.microsoft.com/en-us/library/Ff536962(v=VS.85).aspx">IPropertyStore::GetValue</a> asks each of the provided property stores for the value. The multiplex property store stops searching when one of the property stores returns a success code and a non-VT_EMPTY value. Failure codes cause the search to end and are passed back to the calling application.

The multiplex property store implementation of <a href="https://msdn.microsoft.com/library/Bb761454(v=VS.85).aspx">IPropertyStoreCapabilities::IsPropertyWritable</a> delegates the call to the first store that implements <a href="https://msdn.microsoft.com/en-us/library/Bb761452(v=VS.85).aspx">IPropertyStoreCapabilities</a>. If multiple stores implement <b>IPropertyStoreCapabilities</b>, the subsequent ones are ignored. If no store implements <b>IPropertyStoreCapabilities</b>, this method returns <b>S_OK</b>.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="https://msdn.microsoft.com/en-us/library/Bb776490(v=VS.85).aspx">PSCreateMultiplexPropertyStore</a> in an implementation of <a href="https://msdn.microsoft.com/library/Bb761447(v=VS.85).aspx">IPropertyStoreFactory::GetPropertyStore</a>.


```cpp
// CMyFactory is a reference counted COM object that implements 
// both IPropertyStoreFactory.

// CMyFactory is assumed to be fully implemented, but for the sake of brevity, 
// many functions are not shown here.

// Private functions are prefixed with an underscore.
 
// CMyFactory implementation for IPropertyStoreFactory::GetPropertyStore.
HRESULT CMyFactory::GetPropertyStore(__in GETPROPERTYSTOREFLAGS flags,
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
 
        // CMyFactory multiplexes two property stores.
        IPropertyStore *ppsFirst;
        
        hr = _CreateFirstStore(IID_PPV_ARGS(&ppsFirst));
        
        if (SUCCEEDED(hr))
        {
            IPropertyStore *ppsSecond;
            
            hr = _CreateSecondStore(IID_PPV_ARGS(&ppsSecond));
            
            if (SUCCEEDED(hr))
            {
                IUnknown *rgStores[] = {ppsFirst, ppsSecond};
            
                hr = PSCreateMultiplexPropertyStore(rgStores, ARRAYSIZE(rgStores), riid, ppv);
            
                ppsSecond->Release();
            }
            ppsFirst->Release();
        }
    }
    return hr;
}
```





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb761450(v=VS.85).aspx">IPropertyStoreFactory</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776488(v=VS.85).aspx">PSCreateDelayedMultiplexPropertyStore</a>
 

 


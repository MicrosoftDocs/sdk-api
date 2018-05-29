---
UID: NF:propsys.PSCreateDelayedMultiplexPropertyStore
title: PSCreateDelayedMultiplexPropertyStore function
author: windows-sdk-content
description: Creates a read-only, delayed-binding property store that contains multiple property stores.
old-location: properties\PSCreateDelayedMultiplexPropertyStore.htm
old-project: properties
ms.assetid: 8b264d7e-6124-4724-8d23-605101705893
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: PSCreateDelayedMultiplexPropertyStore, PSCreateDelayedMultiplexPropertyStore function [Windows Properties], _shell_PSCreateDelayedMultiplexPropertyStore, properties.PSCreateDelayedMultiplexPropertyStore, propsys/PSCreateDelayedMultiplexPropertyStore, shell.PSCreateDelayedMultiplexPropertyStore
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: PSC_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Propsys.dll
api_name:
-	PSCreateDelayedMultiplexPropertyStore
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PSCreateDelayedMultiplexPropertyStore function


## -description


Creates a read-only, delayed-binding property store that contains multiple property stores.


## -parameters




### -param flags

Type: <b><a href="shell.GETPROPERTYSTOREFLAGS">GETPROPERTYSTOREFLAGS</a></b>

One or more <a href="shell.GETPROPERTYSTOREFLAGS">GETPROPERTYSTOREFLAGS</a> values. These values specify details of the created property store object.


### -param pdpsf

Type: <b><a href="https://msdn.microsoft.com/855c9f10-9f40-4c60-a669-551fa51133f5">IDelayedPropertyStoreFactory</a>*</b>

Interface pointer to an instance of <a href="https://msdn.microsoft.com/855c9f10-9f40-4c60-a669-551fa51133f5">IDelayedPropertyStoreFactory</a>.


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

When this function returns, contains the interface pointer requested in <i>riid</i>. This is typically <a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function creates a Component Object Model (COM) object that implements <a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a>, 
 <a href="https://msdn.microsoft.com/5f7997ba-a5c8-42b5-90c8-5cb34afd6092">INamedPropertyStore</a>, <a href="https://msdn.microsoft.com/477991e5-0882-475c-9178-c3add695dc2c">IObjectProvider</a>, and <a href="shell.IPropertyStoreCapabilities">IPropertyStoreCapabilities</a>.

Applications must call this object from only one thread at a time.

You must initialize COM with <a href="https://msdn.microsoft.com/0f171cf4-87b9-43a6-97f2-80ed344fe376">CoInitialize</a> or <a href="https://msdn.microsoft.com/9a13e7a0-f2e2-466b-98f5-38d5972fa391">OleInitialize</a> before you call <a href="shell.PSCreateDelayedMultiplexPropertyStore">PSCreateDelayedMultiplexPropertyStore</a>. COM must remain initialized for the lifetime of this object.


<a href="shell.PSCreateDelayedMultiplexPropertyStore">PSCreateDelayedMultiplexPropertyStore</a> is designed as an alternative to <a href="shell.PSCreateMultiplexPropertyStore">PSCreateMultiplexPropertyStore</a>, which requires that the array of property stores be initialized before it creates the multiplex property store.

The delayed binding mechanism is designed as a performance enhancement for calls to <a href="https://msdn.microsoft.com/library/windows/hardware/ff536962">IPropertyStore::GetValue</a> on a multiplex property store. When asked for the value of a property, the delayed multiplex property store checks each of the property stores for the value. After the value is found, there is no need to create and initialize subsequent stores. The delayed multiplex property store stops searching for a value when one of the property stores returns a success code and a non-VT_EMPTY value.

When the delayed multiplex property store needs to access a particular property store, it first checks to see if it has already obtained an interface to that property store. If not, it calls <a href="https://msdn.microsoft.com/26df5fec-2a21-454e-9539-877c00a4f8fb">IDelayedPropertyStoreFactory::GetDelayedPropertyStore</a> with the appropriate property store ID to obtain the property store. It always uses the property store IDs in the order in which they are provided by the application. It is possible that not all IDs will be used.

If the call to <a href="https://msdn.microsoft.com/855c9f10-9f40-4c60-a669-551fa51133f5">IDelayedPropertyStoreFactory</a> fails with E_NOTIMPL or E_ACCESSDENIED for a particular property store ID, or if the application specified <a href="shell.GETPROPERTYSTOREFLAGS">GPS_BESTEFFORT</a>, then the failure is ignored and the delayed multiplex property store moves on to the next property store.

In some cases, it might be beneficial to use <a href="shell.PSCreateDelayedMultiplexPropertyStore">PSCreateDelayedMultiplexPropertyStore</a> in place of <a href="shell.PSCreateMultiplexPropertyStore">PSCreateMultiplexPropertyStore</a>. For example, if an application needs to multiplex two property stores and the first property store is not memory-intensive to initialize and provides PKEY_Size information. Often, calling applications ask for a multiplex property store and then ask for only PKEY_Size before they release the object. In such a case, the application could avoid the cost of initializing the second property store by calling <b>PSCreateDelayedMultiplexPropertyStore</b> and implementing <a href="https://msdn.microsoft.com/855c9f10-9f40-4c60-a669-551fa51133f5">IDelayedPropertyStoreFactory</a>.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.PSCreateDelayedMultiplexPropertyStore">PSCreateDelayedMultiplexPropertyStore</a> in an implementation of <a href="shell.IPropertyStoreFactory_GetPropertyStore">IPropertyStoreFactory::GetPropertyStore</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// CMyFactory is a reference-counted COM object that implements both IPropertyStoreFactory and IDelayedPropertyStoreFactory.

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
    if (flags &amp; GPS_READWRITE)
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
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.IPropertyStoreFactory">IPropertyStoreFactory</a>



<a href="shell.PSCreateMultiplexPropertyStore">PSCreateMultiplexPropertyStore</a>
 

 


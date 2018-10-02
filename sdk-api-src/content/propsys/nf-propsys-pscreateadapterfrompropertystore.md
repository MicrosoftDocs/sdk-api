---
UID: NF:propsys.PSCreateAdapterFromPropertyStore
title: PSCreateAdapterFromPropertyStore function
author: windows-sdk-content
description: Creates an adapter from an IPropertyStore.
old-location: properties\PSCreateAdapterFromPropertyStore.htm
tech.root: properties
ms.assetid: a3489f95-e790-481a-af6e-f30527dc476c
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: PSCreateAdapterFromPropertyStore, PSCreateAdapterFromPropertyStore function [Windows Properties], _shell_PSCreateAdapterFromPropertyStore, properties.PSCreateAdapterFromPropertyStore, propsys/PSCreateAdapterFromPropertyStore, shell.PSCreateAdapterFromPropertyStore
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
 - PSCreateAdapterFromPropertyStore
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# PSCreateAdapterFromPropertyStore function


## -description


Creates an adapter from an <a href="shell.IPropertyStore">IPropertyStore</a>.


## -parameters




### -param pps [in]

Type: <b><a href="shell.IPropertyStore">IPropertyStore</a>*</b>

Pointer to an <a href="shell.IPropertyStore">IPropertyStore</a> object that represents the property store.


### -param riid [in]

Type: <b>REFIID</b>

Reference to an IID.


### -param ppv [out]

Type: <b>void**</b>

When this function returns, contains the interface pointer requested in <i>riid</i>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The adapter object implements <a href="https://msdn.microsoft.com/0ea3e1e0-c135-4138-81e4-f72412fc3128">IPropertySetStorage</a>, <a href="shell.IPropertyStore">IPropertyStore</a>, <a href="shell.IPropertyStoreCapabilities">IPropertyStoreCapabilities</a>, and <a href="https://msdn.microsoft.com/477991e5-0882-475c-9178-c3add695dc2c">IObjectProvider</a>.

Use this function if you need an object that implements <a href="shell.IPropertyStore">IPropertyStore</a> with an API that requires an <a href="https://msdn.microsoft.com/0ea3e1e0-c135-4138-81e4-f72412fc3128">IPropertySetStorage</a> interface. The object created can also be useful to a namespace extension that wants to provide support for binding to namespace items using <b>IPropertySetStorage</b>. Applications must call this object from only one thread at a time.

The adapter property store created by this function retains a reference to the source <a href="shell.IPropertyStore">IPropertyStore</a> interface. Therefore, the calling application is free to release its reference to the source <b>IPropertyStore</b> whenever convenient after calling this function.

The adapter property store makes calls to methods on the <a href="shell.IPropertyStore">IPropertyStore</a> interface as appropriate. Therefore, if the calling application is writing values to the store, it should call the <a href="shell.IPropertyStore_Commit">IPropertyStore::Commit</a> method on only one of the interfaces.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.PSCreateAdapterFromPropertyStore">PSCreateAdapterFromPropertyStore</a> to use an adapter property store to convert an <a href="shell.IPropertyStore">IPropertyStore</a> interface into an <a href="https://msdn.microsoft.com/0ea3e1e0-c135-4138-81e4-f72412fc3128">IPropertySetStorage</a> interface.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// IPropertyStore *ppropstore;
// Assume variable ppropstore is initialized and valid
IPropertySetStorage *pSetStorage;

HRESULT hr = PSCreateadapterFromPropertyStore(ppropstore, IID_PPV_ARGS(&amp;pSetStorage));

if (SUCCEEDED(hr))
{
    // pSetStorage is now valid and can be used to access the data in ppropstore.
    pSetStorage-&gt;Release();
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/0ea3e1e0-c135-4138-81e4-f72412fc3128">IPropertySetStorage</a>



<a href="shell.IPropertyStore">IPropertyStore</a>



<a href="shell.PSCreatePropertyStoreFromPropertySetStorage">PSCreatePropertyStoreFromPropertySetStorage</a>
 

 


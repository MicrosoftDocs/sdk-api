---
UID: NN:functiondiscoveryprovider.IProviderProperties
title: IProviderProperties (functiondiscoveryprovider.h)
author: windows-sdk-content
description: Is optionally implemented by discovery providers to directly create and manage their own property store.
old-location: ncd\iproviderproperties.htm
tech.root: FunDisc
ms.assetid: d6d3d1d1-d2fb-409c-be37-3cd286e325a3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IProviderProperties, IProviderProperties interface, IProviderProperties interface,described, functiondiscoveryprovider/IProviderProperties, ncd.iproviderproperties
ms.topic: interface
req.header: functiondiscoveryprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FunctionDiscoveryProvider.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FunctionDiscoveryProvider.h
api_name:
 - IProviderProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IProviderProperties interface


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

This interface is optionally implemented by discovery providers to directly create and manage their own property store. If this interface is implemented, the provider can use its property store for its own internal use, but all queries from the property store implemented by this interface will go directly to the provider, and the internal property store will never be exposed to a client calling <a href="https://msdn.microsoft.com/3e03567b-7bac-4bef-ae62-a040f0c33cfb">IFunctionInstance::OpenPropertyStore</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IProviderProperties</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IProviderProperties</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IProviderProperties</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f76d010b-f9dd-46d7-9b1f-eba3d11aaef1">GetAt</a>
</td>
<td align="left" width="63%">
Gets the property key at the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/25ed5782-c19e-4c3d-81f1-74e0ea3e195e">GetCount</a>
</td>
<td align="left" width="63%">
Gets the number of properties in the property store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c32a5367-ef39-4852-bf3b-203d27d0a2d0">GetValue</a>
</td>
<td align="left" width="63%">
Gets the value of the specified property key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5aa3e6a3-febc-4d2d-b58b-abfad28d325d">SetValue</a>
</td>
<td align="left" width="63%">
Sets the value of the specified property key.

</td>
</tr>
</table> 


## -remarks



Implementing this interface enables a provider to provide access to the most current property values. Otherwise, the client uses the values in the cache created by Function Discovery when the function instance is created or the property store is opened.

If a provider does not implement this interface, then the provider must provide a property store
at the time the instance is created or when the client calls <a href="https://msdn.microsoft.com/35e98e8a-5e6c-4cbb-9a61-9720f11f90d6">InstancePropertyStoreOpen</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb761474(v=VS.85).aspx">IPropertyStore</a>
 

 


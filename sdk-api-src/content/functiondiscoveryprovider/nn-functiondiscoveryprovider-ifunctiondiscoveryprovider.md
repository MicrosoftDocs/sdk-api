---
UID: NN:functiondiscoveryprovider.IFunctionDiscoveryProvider
title: IFunctionDiscoveryProvider
author: windows-driver-content
description: This is the main interface implemented by a discovery provider. It is the primary interface the Function Discovery infrastructure uses to communicate with the provider and its resources.
old-location: ncd\ifunctiondiscoveryprovider.htm
old-project: FunDisc
ms.assetid: e0019d0d-1495-4a0e-a7d9-7772046a4a26
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IFunctionDiscoveryProvider, IFunctionDiscoveryProvider interface, IFunctionDiscoveryProvider interface,described, functiondiscoveryprovider/IFunctionDiscoveryProvider, ncd.ifunctiondiscoveryprovider
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: PropertyConstraint
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	FunctionDiscoveryProvider.h
api_name:
-	IFunctionDiscoveryProvider
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# IFunctionDiscoveryProvider interface


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

This is the main interface implemented by a discovery provider. It is the primary interface the Function Discovery infrastructure uses to communicate with the provider and its resources.

You should only implement and use this interface if you are writing a discovery provider. You should only write a discovery provider if you must discover devices using a method that is not supported by the <a href="https://msdn.microsoft.com/45caf8f6-3173-4b1a-bbbe-66637ac1f7bc">built-in providers</a>.  

If you are writing a client program that discovers and queries devices, use the <a href="https://msdn.microsoft.com/352a8d61-7d3a-423d-8b7e-1163d4fa1e00">IFunctionDiscovery</a> interface instead.

The <a href="https://msdn.microsoft.com/81955209-d6e2-49a2-ad41-55612b3eb430">Function Discovery Provider Sample</a> implements the <b>IFunctionDiscoveryProvider</b> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFunctionDiscoveryProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IFunctionDiscoveryProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFunctionDiscoveryProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/be19f2ac-037c-443b-b36f-68b9c9f132f8">EndQuery</a>
</td>
<td align="left" width="63%">
Terminates a query being executed by a provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the Function Discovery provider object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7ad29f46-fb21-4287-9fc9-9ab86d44d298">InstancePropertyStoreFlush</a>
</td>
<td align="left" width="63%">
Provides a mechanism for the provider to persist properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/35e98e8a-5e6c-4cbb-9a61-9720f11f90d6">InstancePropertyStoreOpen</a>
</td>
<td align="left" width="63%">
Opens the property store of the provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0ee8d65d-0be3-4171-946a-10a15b8f8eb7">InstancePropertyStoreValidateAccess</a>
</td>
<td align="left" width="63%">
Verifies that the provider supports the  requested access.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8fb955dd-f396-4473-a1c1-b0d83e2b4b07">InstanceQueryService</a>
</td>
<td align="left" width="63%">
Creates a COM object for the function instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fa348767-8a83-4a45-9411-1e9eb545d97d">InstanceReleased</a>
</td>
<td align="left" width="63%">
Releases the specified function instance and frees the memory previously allocated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406403">Query</a>
</td>
<td align="left" width="63%">
Retrieves a collection of function instances that meet the specified constraints.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/81955209-d6e2-49a2-ad41-55612b3eb430">Function Discovery Provider Sample</a>



<a href="https://msdn.microsoft.com/26660093-0d02-4eef-bf5b-18ff07748540">Using Function Discovery Providers</a>
 

 


---
UID: NN:functiondiscoveryprovider.IFunctionDiscoveryProviderFactory
title: IFunctionDiscoveryProviderFactory
author: windows-sdk-content
description: Provides factory methods to create Function Discovery objects.
old-location: ncd\ifunctiondiscoveryproviderfactory.htm
old-project: FunDisc
ms.assetid: 576db617-0bca-4b46-839b-0f133f28cacb
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IFunctionDiscoveryProviderFactory, IFunctionDiscoveryProviderFactory interface, IFunctionDiscoveryProviderFactory interface,described, functiondiscoveryprovider/IFunctionDiscoveryProviderFactory, ncd.ifunctiondiscoveryproviderfactory
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: PropertyConstraint
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FunctionDiscoveryProvider.h
api_name:
 - IFunctionDiscoveryProviderFactory
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# IFunctionDiscoveryProviderFactory interface


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Provides factory methods to create Function Discovery objects.

Synchronous query results are passed using the <a href="https://msdn.microsoft.com/8ac1a406-92f3-4e39-985e-ab8fa7d28751">IFunctionInstanceCollection</a> parameter of <a href="https://msdn.microsoft.com/8c368ea7-c9db-4e80-a080-eef8068f7402">IFunctionDiscoveryProvider::Query</a> method.  


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFunctionDiscoveryProviderFactory</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IFunctionDiscoveryProviderFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFunctionDiscoveryProviderFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c49f6be1-1789-4415-8898-ad74e0148c47">CreateFunctionInstanceCollection</a>
</td>
<td align="left" width="63%">
Creates a function instance collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/143a4f62-7093-4127-b89e-e7d0985a92bb">CreateInstance</a>
</td>
<td align="left" width="63%">
Creates a function instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/668d0a70-a0c1-4e43-a258-5221e3fe28a1">CreatePropertyStore</a>
</td>
<td align="left" width="63%">
Enables providers to reuse the in-memory property store implementation.

</td>
</tr>
</table> 


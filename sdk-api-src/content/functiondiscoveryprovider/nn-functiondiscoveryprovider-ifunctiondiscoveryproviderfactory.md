---
UID: NN:functiondiscoveryprovider.IFunctionDiscoveryProviderFactory
title: IFunctionDiscoveryProviderFactory (functiondiscoveryprovider.h)
author: windows-sdk-content
description: Provides factory methods to create Function Discovery objects.
old-location: ncd\ifunctiondiscoveryproviderfactory.htm
tech.root: FunDisc
ms.assetid: 576db617-0bca-4b46-839b-0f133f28cacb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFunctionDiscoveryProviderFactory, IFunctionDiscoveryProviderFactory interface, IFunctionDiscoveryProviderFactory interface,described, functiondiscoveryprovider/IFunctionDiscoveryProviderFactory, ncd.ifunctiondiscoveryproviderfactory
ms.topic: interface
f1_keywords: 
 - "functiondiscoveryprovider/IFunctionDiscoveryProviderFactory"
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
 - IFunctionDiscoveryProviderFactory
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFunctionDiscoveryProviderFactory interface


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Provides factory methods to create Function Discovery objects.

Synchronous query results are passed using the <a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctioninstancecollection">IFunctionInstanceCollection</a> parameter of <a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-ifunctiondiscoveryprovider-query">IFunctionDiscoveryProvider::Query</a> method.  


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFunctionDiscoveryProviderFactory</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFunctionDiscoveryProviderFactory</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-ifunctiondiscoveryproviderfactory-createfunctioninstancecollection">CreateFunctionInstanceCollection</a>
</td>
<td align="left" width="63%">
Creates a function instance collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-ifunctiondiscoveryproviderfactory-createinstance">CreateInstance</a>
</td>
<td align="left" width="63%">
Creates a function instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-ifunctiondiscoveryproviderfactory-createpropertystore">CreatePropertyStore</a>
</td>
<td align="left" width="63%">
Enables providers to reuse the in-memory property store implementation.

</td>
</tr>
</table> 


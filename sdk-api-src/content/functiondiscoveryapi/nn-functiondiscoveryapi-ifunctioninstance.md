---
UID: NN:functiondiscoveryapi.IFunctionInstance
title: IFunctionInstance (functiondiscoveryapi.h)
author: windows-sdk-content
description: A function instance is created as the result of calling one of the IFunctionDiscovery methods; client program do not create these objects themselves.
old-location: ncd\ifunctioninstance.htm
tech.root: FunDisc
ms.assetid: cc421719-73a6-4d4d-9bf8-171e46c4e275
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFunctionInstance, IFunctionInstance interface, IFunctionInstance interface,described, functiondiscoveryapi/IFunctionInstance, ncd.ifunctioninstance
ms.topic: interface
f1_keywords: ["functiondiscoveryapi/IFunctionInstance"]
req.header: functiondiscoveryapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FunctionDiscoveryAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: FunDisc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FunDisc.dll
api_name:
 - IFunctionInstance
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFunctionInstance interface


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

    A function instance is created as the result of calling one of the <a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctiondiscovery">IFunctionDiscovery</a>  methods; client program do not create these objects themselves.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFunctionInstance</b> interface inherits from <b>IServiceProvider</b>. <b>IFunctionInstance</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFunctionInstance</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctioninstance-getcategory">GetCategory</a>
</td>
<td align="left" width="63%">
Gets the category and subcategory strings for the function instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctioninstance-getid">GetID</a>
</td>
<td align="left" width="63%">
Gets the identifier string for the function instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctioninstance-getproviderinstanceid">GetProviderInstanceID</a>
</td>
<td align="left" width="63%">
Gets the identifier string for the provider instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctioninstance-openpropertystore">OpenPropertyStore</a>
</td>
<td align="left" width="63%">
Opens the property store for the function instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa364381(v=vs.85)">QueryService</a>
</td>
<td align="left" width="63%">
Acts as the factory method for any services exposed through an implementation of <b>IFunctionInstance</b>.

</td>
</tr>
</table> 


---
UID: NN:functiondiscoveryprovider.IFunctionDiscoveryProvider
title: IFunctionDiscoveryProvider (functiondiscoveryprovider.h)
description: This is the main interface implemented by a discovery provider. It is the primary interface the Function Discovery infrastructure uses to communicate with the provider and its resources.
helpviewer_keywords: ["IFunctionDiscoveryProvider","IFunctionDiscoveryProvider interface","IFunctionDiscoveryProvider interface","described","functiondiscoveryprovider/IFunctionDiscoveryProvider","ncd.ifunctiondiscoveryprovider"]
old-location: ncd\ifunctiondiscoveryprovider.htm
tech.root: FunDisc
ms.assetid: e0019d0d-1495-4a0e-a7d9-7772046a4a26
ms.date: 12/05/2018
ms.keywords: IFunctionDiscoveryProvider, IFunctionDiscoveryProvider interface, IFunctionDiscoveryProvider interface,described, functiondiscoveryprovider/IFunctionDiscoveryProvider, ncd.ifunctiondiscoveryprovider
f1_keywords:
- functiondiscoveryprovider/IFunctionDiscoveryProvider
dev_langs:
- c++
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
- IFunctionDiscoveryProvider
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFunctionDiscoveryProvider interface


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

This is the main interface implemented by a discovery provider. It is the primary interface the Function Discovery infrastructure uses to communicate with the provider and its resources.

You should only implement and use this interface if you are writing a discovery provider. You should only write a discovery provider if you must discover devices using a method that is not supported by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fundisc/built-in-providers">built-in providers</a>.  

If you are writing a client program that discovers and queries devices, use the <a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctiondiscovery">IFunctionDiscovery</a> interface instead.

The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fundisc/function-discovery-provider-sample">Function Discovery Provider Sample</a> implements the <b>IFunctionDiscoveryProvider</b> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFunctionDiscoveryProvider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFunctionDiscoveryProvider</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-ifunctiondiscoveryprovider-endquery">EndQuery</a>
</td>
<td align="left" width="63%">
Terminates a query being executed by a provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-ifunctiondiscoveryprovider-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the Function Discovery provider object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-ifunctiondiscoveryprovider-instancepropertystoreflush">InstancePropertyStoreFlush</a>
</td>
<td align="left" width="63%">
Provides a mechanism for the provider to persist properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-ifunctiondiscoveryprovider-instancepropertystoreopen">InstancePropertyStoreOpen</a>
</td>
<td align="left" width="63%">
Opens the property store of the provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-ifunctiondiscoveryprovider-instancepropertystorevalidateaccess">InstancePropertyStoreValidateAccess</a>
</td>
<td align="left" width="63%">
Verifies that the provider supports the  requested access.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-ifunctiondiscoveryprovider-instancequeryservice">InstanceQueryService</a>
</td>
<td align="left" width="63%">
Creates a COM object for the function instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-ifunctiondiscoveryprovider-instancereleased">InstanceReleased</a>
</td>
<td align="left" width="63%">
Releases the specified function instance and frees the memory previously allocated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-ifunctiondiscoveryprovider-query">Query</a>
</td>
<td align="left" width="63%">
Retrieves a collection of function instances that meet the specified constraints.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fundisc/function-discovery-provider-sample">Function Discovery Provider Sample</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fundisc/using-function-discovery-providers">Using Function Discovery Providers</a>
 

 


---
UID: NF:functiondiscoveryprovider.IFunctionDiscoveryProvider.EndQuery
title: IFunctionDiscoveryProvider::EndQuery (functiondiscoveryprovider.h)
description: Terminates a query being executed by a provider.
helpviewer_keywords: ["EndQuery","EndQuery method","EndQuery method","IFunctionDiscoveryProvider interface","IFunctionDiscoveryProvider interface","EndQuery method","IFunctionDiscoveryProvider.EndQuery","IFunctionDiscoveryProvider::EndQuery","functiondiscoveryprovider/IFunctionDiscoveryProvider::EndQuery","ncd.ifunctiondiscoveryprovider_endquery_method"]
old-location: ncd\ifunctiondiscoveryprovider_endquery_method.htm
tech.root: ncd
ms.assetid: be19f2ac-037c-443b-b36f-68b9c9f132f8
ms.date: 12/05/2018
ms.keywords: EndQuery, EndQuery method, EndQuery method,IFunctionDiscoveryProvider interface, IFunctionDiscoveryProvider interface,EndQuery method, IFunctionDiscoveryProvider.EndQuery, IFunctionDiscoveryProvider::EndQuery, functiondiscoveryprovider/IFunctionDiscoveryProvider::EndQuery, ncd.ifunctiondiscoveryprovider_endquery_method
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFunctionDiscoveryProvider::EndQuery
 - functiondiscoveryprovider/IFunctionDiscoveryProvider::EndQuery
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FunctionDiscoveryProvider.h
api_name:
 - IFunctionDiscoveryProvider.EndQuery
---

# IFunctionDiscoveryProvider::EndQuery


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Terminates a query being executed by a provider.



## -returns

Possible return values include, but are not limited to, the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters contains an invalid argument.

</td>
</tr>
</table>

## -remarks

This method is called by Function Discovery to indicate to a provider that no further query notifications will be sent to the <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctiondiscoverynotification">IFunctionDiscoveryNotification</a> callback interface. Implementers should try to ensure that no further query notifications are sent to Function Discovery after the call to <b>EndQuery</b> returns. If a provider implementation sends a notification after <b>EndQuery</b>  returns, Function Discovery returns an error to the provider and the notification is not forwarded to the client. 

<b>EndQuery</b> is only called when a client passed an <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctiondiscoverynotification">IFunctionDiscoveryNotification</a> interface passed to the provider's <a href="/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-ifunctiondiscoveryprovider-initialize">Initialize</a> method.

Any data structures associated with the query can be deleted in the implementation of <b>EndQuery</b>. Any private context memory allocated by the <a href="/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-ifunctiondiscoveryprovider-query">Query</a> method should also be deleted.

Note that <a href="/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-ifunctiondiscoveryprovider-query">Query</a> can be invoked again once <b>EndQuery</b> has returned.

## -see-also

<a href="/windows/desktop/api/functiondiscoveryprovider/nn-functiondiscoveryprovider-ifunctiondiscoveryprovider">IFunctionDiscoveryProvider</a>

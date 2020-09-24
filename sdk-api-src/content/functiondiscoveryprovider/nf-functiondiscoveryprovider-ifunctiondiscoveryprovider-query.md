---
UID: NF:functiondiscoveryprovider.IFunctionDiscoveryProvider.Query
title: IFunctionDiscoveryProvider::Query (functiondiscoveryprovider.h)
description: Retrieves a collection of function instances that meet the specified constraints.
helpviewer_keywords: ["IFunctionDiscoveryProvider interface","Query method","IFunctionDiscoveryProvider.Query","IFunctionDiscoveryProvider::Query","Query","Query method","Query method","IFunctionDiscoveryProvider interface","functiondiscoveryprovider/IFunctionDiscoveryProvider::Query","ncd.ifunctiondiscoveryprovider_query_method"]
old-location: ncd\ifunctiondiscoveryprovider_query_method.htm
tech.root: ncd
ms.assetid: 8c368ea7-c9db-4e80-a080-eef8068f7402
ms.date: 12/05/2018
ms.keywords: IFunctionDiscoveryProvider interface,Query method, IFunctionDiscoveryProvider.Query, IFunctionDiscoveryProvider::Query, Query, Query method, Query method,IFunctionDiscoveryProvider interface, functiondiscoveryprovider/IFunctionDiscoveryProvider::Query, ncd.ifunctiondiscoveryprovider_query_method
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
 - IFunctionDiscoveryProvider::Query
 - functiondiscoveryprovider/IFunctionDiscoveryProvider::Query
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
 - IFunctionDiscoveryProvider.Query
---

# IFunctionDiscoveryProvider::Query


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Retrieves a collection of function instances that meet the specified constraints.

## -parameters

### -param pIFunctionDiscoveryProviderQuery [in]

A pointer to an <a href="/windows/desktop/api/functiondiscoveryprovider/nn-functiondiscoveryprovider-ifunctiondiscoveryproviderquery">IFunctionDiscoveryProviderQuery</a>  interface that contains parameters that define the query criteria.

### -param ppIFunctionInstanceCollection [out]

A pointer to an <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctioninstancecollection">IFunctionInstanceCollection</a> interface that the provider should use to return function instances synchronously in response to the given query.

When you implement the <b>Query</b> method, you can set this parameter to <b>NULL</b> if your provider supports notifications, that is, your provider returns results asynchronously. Asynchronous results should be returned using the <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctiondiscoverynotification">IFunctionDiscoveryNotification</a> interface passed to the provider's <a href="/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-ifunctiondiscoveryprovider-initialize">Initialize</a> method.

If the client application has not implemented notifications, it may pass a <b>NULL</b> parameter.

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
The method completed successfully and the results are being returned synchronously.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pIFunctionDiscoveryProviderQuery</i>  parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully and the results are being returned asynchronously.

</td>
</tr>
</table>

## -remarks

An active query is terminated by Function Discovery with a call to the <a href="/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-ifunctiondiscoveryprovider-endquery">EndQuery</a> method.  Note that <b>EndQuery</b> will only be called if the client specified a <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctiondiscoverynotification">IFunctionDiscoveryNotification</a> interface for the query.  If a <b>IFunctionDiscoveryNotification</b> was not provided, the query must be considered ended by the provider once the <b>Query</b> call is complete.

A client can re-execute a query at any time after the previous <b>Query</b> call has returned. The implementation of <b>Query</b> must be able to return an <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctioninstancecollection">IFunctionInstanceCollection</a> for the new query. <a href="/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-ifunctiondiscoveryprovider-endquery">EndQuery</a> will only be called before a subsequent <b>Query</b> call when a client passed an <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctiondiscoverynotification">IFunctionDiscoveryNotification</a> interface passed to the provider's <a href="/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-ifunctiondiscoveryprovider-initialize">Initialize</a> method.

If <b>Query</b> returns <b>E_PENDING</b>, the provider must call the <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctiondiscoverynotification-onevent">OnEvent</a> method of the <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctiondiscoverynotification">IFunctionDiscoveryNotification</a> interface with <b>FD_EVENTID_SEARCHCOMPLETE</b> to indicate that the enumeration of results is complete.  Failure to send the <b>FD_EVENTID_SEARCHCOMPLETE</b> event can result in clients hanging indefinitely

## -see-also

<a href="/windows/desktop/api/functiondiscoveryprovider/nn-functiondiscoveryprovider-ifunctiondiscoveryprovider">IFunctionDiscoveryProvider</a>
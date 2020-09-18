---
UID: NF:functiondiscoveryapi.IFunctionInstanceCollectionQuery.Execute
title: IFunctionInstanceCollectionQuery::Execute (functiondiscoveryapi.h)
description: Performs the query defined by IFunctionDiscovery::CreateInstanceCollectionQuery.
helpviewer_keywords: ["Execute","Execute method","Execute method","IFunctionInstanceCollectionQuery interface","IFunctionInstanceCollectionQuery interface","Execute method","IFunctionInstanceCollectionQuery.Execute","IFunctionInstanceCollectionQuery::Execute","functiondiscoveryapi/IFunctionInstanceCollectionQuery::Execute","ncd.ifunctioninstancecollectionquery_execute_method"]
old-location: ncd\ifunctioninstancecollectionquery_execute_method.htm
tech.root: ncd
ms.assetid: b924d066-87d7-499b-b006-a10e219e11fd
ms.date: 12/05/2018
ms.keywords: Execute, Execute method, Execute method,IFunctionInstanceCollectionQuery interface, IFunctionInstanceCollectionQuery interface,Execute method, IFunctionInstanceCollectionQuery.Execute, IFunctionInstanceCollectionQuery::Execute, functiondiscoveryapi/IFunctionInstanceCollectionQuery::Execute, ncd.ifunctioninstancecollectionquery_execute_method
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFunctionInstanceCollectionQuery::Execute
 - functiondiscoveryapi/IFunctionInstanceCollectionQuery::Execute
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FunDisc.dll
api_name:
 - IFunctionInstanceCollectionQuery.Execute
---

# IFunctionInstanceCollectionQuery::Execute


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Performs the query defined by <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctiondiscovery-createinstancecollectionquery">IFunctionDiscovery::CreateInstanceCollectionQuery</a>.

## -parameters

### -param ppIFunctionInstanceCollection [out]

A pointer to an <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctioninstancecollection">IFunctionInstanceCollection</a> interface pointer that receives the requested function instance collection.

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
The method completed successfully.   Results are returned synchronously in <i>ppIFunctonInstanceCollecton</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method is unable to allocate the memory required to perform this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
Some of the results will be returned by asynchronous notification.  See the remarks for details.

</td>
</tr>
</table>
 

 A predefined query is a query of a layered <a href="/previous-versions/windows/desktop/fundisc/function-discovery-categories">category</a>. When a predefined query is executed, each provider that returns a function instance also returns an HRESULT value. The provider HRESULT values  are aggregated, and the value returned by the <b>Execute</b>  method reflects these aggregate results. Results are aggregated as follows:

<ul>
<li>If all providers return <b>S_OK</b>, <b>Execute</b>   returns <b>S_OK</b>.</li>
<li>If at least one provider returns <b>E_PENDING</b>, and all other providers return either <b>S_OK</b> or <b>E_PENDING</b>, <b>Execute</b>   returns <b>E_PENDING</b>.</li>
<li>If all providers return an error value (that is, a value other than <b>S_OK</b> or <b>E_PENDING</b>), <b>Execute</b> returns the error value returned by the network provider that was last queried. Also, if the client's  <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctiondiscoverynotification">IFunctionDiscoveryNotification</a> callback routine was provided to <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctiondiscovery-createinstancecollectionquery">IFunctionDiscovery::CreateInstanceCollectionQuery</a>, an <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctiondiscoverynotification-onerror">OnError</a>  notification is sent for each provider. Each   <b>OnError</b> notification contains the HRESULT returned by the provider.</li>
<li>If at least one provider returns an error value, and all other providers return <b>S_OK</b>, <b>Execute</b>   returns <b>S_OK</b>. <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctiondiscoverynotification-onerror">OnError</a>  notifications are sent as described above.</li>
<li>If at least one provider returns an error value, and at least one provider returns <b>E_PENDING</b>, <b>Execute</b> returns <b>E_PENDING</b>.  <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctiondiscoverynotification-onerror">OnError</a> notifications are sent as described above.</li>
</ul>
When <b>Execute</b> returns <b>S_OK</b>, <i>ppIFunctionInstanceCollection</i> contains the results of the query.  If an <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctiondiscoverynotification">IFunctionDiscoveryNotification</a> interface is provided to the <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctiondiscovery-createinstancecollectionquery">CreateInstanceCollectionQuery</a> method of  <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctiondiscovery">IFunctionDiscovery</a>, then changes to the results will be communicated using that interface.

When <b>Execute</b> returns <b>E_PENDING</b>, the result set will be returned asynchronously through the <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctiondiscoverynotification">IFunctionDiscoveryNotification</a> interface provided to the <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctiondiscovery-createinstancecollectionquery">CreateInstanceCollectionQuery</a> method of <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctiondiscovery">IFunctionDiscovery</a>.  <i>ppIFunctionInstanceCollection</i> may be <b>NULL</b> or may contain a partial result set.  The enumeration is complete once the <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctiondiscoverynotification-onevent">OnEvent</a> method of  <b>IFunctionDiscoveryNotification</b> is called with <b>FD_EVENTID_SEARCHCOMPLETE</b>.  After the <b>FD_EVENTID_SEARCHCOMPLETE</b> event is received, additional notifications are updates to the results.

## -remarks

This method must be must be invoked by the client program before any data can be retrieved from the query object. When called, this method performs the following: 

<ol>
<li>Retrieves the function instance collection object.</li>
<li>Queries the provider of the category that is passed into <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctiondiscovery-createinstancecollectionquery">IFunctionDiscovery::CreateInstanceCollectionQuery</a>.</li>
<li>Retrieves the category provider.</li>
<li>Queries the category provider  using the subcategory data to generate the collection using query constraints.</li>
<li>Initiates the update notification mechanism if the address of the client program's <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctiondiscoverynotification">IFunctionDiscoveryNotification</a> callback routine is provided to <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctiondiscovery-createinstancecollectionquery">IFunctionDiscovery::CreateInstanceCollectionQuery</a>.</li>
<li>Caches the collection data and returns.</li>
</ol>
Function Discovery network providers only return function instances through the <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctiondiscoverynotification">IFunctionDiscoveryNotification</a> interface.  They return no function instances directly when this method is invoked. Instead, <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctioninstancequery-execute">Execute</a> simply initiates an entirely asynchronous retrieval operation and returns <b>E_PENDING</b> to indicate that the results will be returned asynchronously.   Notifications must be used to retrieve function instances from Function Discovery network providers.

## -see-also

<a href="/previous-versions/windows/desktop/fundisc/function-discovery-queries">Function Discovery Queries</a>



<a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctioninstancecollectionquery">IFunctionInstanceCollectionQuery</a>
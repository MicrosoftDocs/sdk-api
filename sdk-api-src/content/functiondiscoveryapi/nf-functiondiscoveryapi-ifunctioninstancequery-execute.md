---
UID: NF:functiondiscoveryapi.IFunctionInstanceQuery.Execute
title: IFunctionInstanceQuery::Execute (functiondiscoveryapi.h)
description: Performs the query defined by IFunctionDiscovery::CreateInstanceQuery.
helpviewer_keywords: ["Execute","Execute method","Execute method","IFunctionInstanceQuery interface","IFunctionInstanceQuery interface","Execute method","IFunctionInstanceQuery.Execute","IFunctionInstanceQuery::Execute","functiondiscoveryapi/IFunctionInstanceQuery::Execute","ncd.ifunctioninstancequery_execute_method"]
old-location: ncd\ifunctioninstancequery_execute_method.htm
tech.root: ncd
ms.assetid: 42618944-6ae6-45f0-85f9-3c958d719ed2
ms.date: 12/05/2018
ms.keywords: Execute, Execute method, Execute method,IFunctionInstanceQuery interface, IFunctionInstanceQuery interface,Execute method, IFunctionInstanceQuery.Execute, IFunctionInstanceQuery::Execute, functiondiscoveryapi/IFunctionInstanceQuery::Execute, ncd.ifunctioninstancequery_execute_method
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
 - IFunctionInstanceQuery::Execute
 - functiondiscoveryapi/IFunctionInstanceQuery::Execute
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
 - IFunctionInstanceQuery.Execute
---

# IFunctionInstanceQuery::Execute


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Performs the query defined by <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctiondiscovery-createinstancequery">IFunctionDiscovery::CreateInstanceQuery</a>.

## -parameters

### -param ppIFunctionInstance [out]

A pointer to an <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctioninstance">IFunctionInstance</a> interface pointer that receives the requested function instance.

## -returns

Possible return values include, but are not limited to, the following.

<table>
<tr>
<th>Return code/value</th>
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
The <i>ppIFunctionInstance</i> parameter is <b>NULL</b>.

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
The results to be returned by a provider will come through asynchronous notification.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_OBJECT_NOT_FOUND)</b></dt>
<dt>0x800710d8</dt>
</dl>
</td>
<td width="60%">
The function instance represented by the specified ID does not exist on this computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_KEY_DELETED)</b></dt>
<dt>0x800703fa</dt>
</dl>
</td>
<td width="60%">
The function instance could not be returned because the key corresponding to the function instance was deleted by another process. This error is returned by the registry provider if a key is deleted while query processing is taking place.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)</b></dt>
<dt>0x80070002</dt>
</dl>
</td>
<td width="60%">
The function instance could not be returned because the key corresponding to the function instance could not be found. This error is returned by the registry provider when the provider could not find matching instances for an instance query.

</td>
</tr>
</table>
 

A predefined query is a query of a layered <a href="/previous-versions/windows/desktop/fundisc/function-discovery-categories">category</a>. When a predefined query is executed, each provider that returns a function instance also returns an HRESULT value. The provider HRESULT values  are aggregated, and the value returned by the <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctioninstancecollectionquery-execute">Execute</a>  method reflects these aggregate results. Results are aggregated as follows:

<ul>
<li>If all providers return S_OK, <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctioninstancecollectionquery-execute">Execute</a>   returns S_OK.</li>
<li>If at least one provider returns E_PENDING, and all other providers return either S_OK or E_PENDING, <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctioninstancecollectionquery-execute">Execute</a>   returns E_PENDING.</li>
<li>If all providers return an error value (that is, a value other than S_OK or E_PENDING), <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctioninstancecollectionquery-execute">Execute</a> returns the error value returned by the network provider that was last queried. Also, if the client's  <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctiondiscoverynotification">IFunctionDiscoveryNotification</a> callback routine was provided to <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctiondiscovery-createinstancecollectionquery">IFunctionDiscovery::CreateInstanceCollectionQuery</a>, an <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctiondiscoverynotification-onerror">OnError</a>  notification is sent for each provider. Each   <b>OnError</b> notification contains the HRESULT returned by the provider.</li>
<li>If at least one provider returns an error value, and all other providers return S_OK, <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctioninstancecollectionquery-execute">Execute</a>   returns S_OK. <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctiondiscoverynotification-onerror">OnError</a>  notification(s) are sent as described above.</li>
<li>If at least one provider returns an error value, and at least one provider returns E_PENDING, <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctioninstancecollectionquery-execute">Execute</a> returns E_PENDING.  <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctiondiscoverynotification-onerror">OnError</a> notification(s) are sent as described above.</li>
</ul>

## -remarks

This method must be must be invoked by the client program to retrieve data from the query object. When called, this method performs the following: 

<ol>
<li>Retrieves the function instance.</li>
<li>Initiates the update notification mechanism if the address of the client program's <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctiondiscoverynotification">IFunctionDiscoveryNotification</a> callback routine is provided to <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctiondiscovery-createinstancequery">IFunctionDiscovery::CreateInstanceQuery</a>.</li>
</ol>
Function Discovery network providers only return function instances through the <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctiondiscoverynotification">IFunctionDiscoveryNotification</a> interface.  They return no function instances directly when this method is invoked. Instead, <b>Execute</b> simply initiates an entirely asynchronous retrieval operation and returns E_PENDING to indicate that the results will be returned asynchronously.   Notifications must be used to retrieve function instances from Function Discovery network providers.

If <b>Execute</b> is called twice on the same query object, the first query is terminated before the second query executes.

## -see-also

<a href="/previous-versions/windows/desktop/fundisc/function-discovery-queries">Function Discovery Queries</a>



<a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctioninstancequery">IFunctionInstanceQuery</a>
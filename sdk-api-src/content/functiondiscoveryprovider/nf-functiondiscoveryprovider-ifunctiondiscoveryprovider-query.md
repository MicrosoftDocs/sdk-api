---
UID: NF:functiondiscoveryprovider.IFunctionDiscoveryProvider.Query
title: IFunctionDiscoveryProvider::Query
author: windows-sdk-content
description: Retrieves a collection of function instances that meet the specified constraints.
old-location: ncd\ifunctiondiscoveryprovider_query_method.htm
tech.root: fundisc
ms.assetid: 8c368ea7-c9db-4e80-a080-eef8068f7402
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFunctionDiscoveryProvider interface,Query method, IFunctionDiscoveryProvider.Query, IFunctionDiscoveryProvider::Query, Query, Query method, Query method,IFunctionDiscoveryProvider interface, functiondiscoveryprovider/IFunctionDiscoveryProvider::Query, ncd.ifunctiondiscoveryprovider_query_method
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IFunctionDiscoveryProvider.Query
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFunctionDiscoveryProvider::Query


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Retrieves a collection of function instances that meet the specified constraints.


## -parameters




### -param pIFunctionDiscoveryProviderQuery [in]

A pointer to an <a href="https://msdn.microsoft.com/97468045-faa5-4690-8db5-50ee9656517b">IFunctionDiscoveryProviderQuery</a>  interface that contains parameters that define the query criteria.


### -param ppIFunctionInstanceCollection [out]

A pointer to an <a href="https://msdn.microsoft.com/8ac1a406-92f3-4e39-985e-ab8fa7d28751">IFunctionInstanceCollection</a> interface that the provider should use to return function instances synchronously in response to the given query.

When you implement the <b>Query</b> method, you can set this parameter to <b>NULL</b> if your provider supports notifications, that is, your provider returns results asynchronously. Asynchronous results should be returned using the <a href="https://msdn.microsoft.com/1819fe08-b151-482d-8e2c-1d599fd15609">IFunctionDiscoveryNotification</a> interface passed to the provider's <a href="https://msdn.microsoft.com/084d6d91-4637-4325-887b-e9f46ecaaee4">Initialize</a> method.

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



An active query is terminated by Function Discovery with a call to the <a href="https://msdn.microsoft.com/be19f2ac-037c-443b-b36f-68b9c9f132f8">EndQuery</a> method.  Note that <b>EndQuery</b> will only be called if the client specified a <a href="https://msdn.microsoft.com/1819fe08-b151-482d-8e2c-1d599fd15609">IFunctionDiscoveryNotification</a> interface for the query.  If a <b>IFunctionDiscoveryNotification</b> was not provided, the query must be considered ended by the provider once the <b>Query</b> call is complete.

A client can re-execute a query at any time after the previous <b>Query</b> call has returned. The implementation of <b>Query</b> must be able to return an <a href="https://msdn.microsoft.com/8ac1a406-92f3-4e39-985e-ab8fa7d28751">IFunctionInstanceCollection</a> for the new query. <a href="https://msdn.microsoft.com/be19f2ac-037c-443b-b36f-68b9c9f132f8">EndQuery</a> will only be called before a subsequent <b>Query</b> call when a client passed an <a href="https://msdn.microsoft.com/1819fe08-b151-482d-8e2c-1d599fd15609">IFunctionDiscoveryNotification</a> interface passed to the provider's <a href="https://msdn.microsoft.com/084d6d91-4637-4325-887b-e9f46ecaaee4">Initialize</a> method.

If <b>Query</b> returns <b>E_PENDING</b>, the provider must call the <a href="https://msdn.microsoft.com/4ebfdf15-ca37-4905-b842-8854a0bd276b">OnEvent</a> method of the <a href="https://msdn.microsoft.com/1819fe08-b151-482d-8e2c-1d599fd15609">IFunctionDiscoveryNotification</a> interface with <b>FD_EVENTID_SEARCHCOMPLETE</b> to indicate that the enumeration of results is complete.  Failure to send the <b>FD_EVENTID_SEARCHCOMPLETE</b> event can result in clients hanging indefinitely




## -see-also




<a href="https://msdn.microsoft.com/e0019d0d-1495-4a0e-a7d9-7772046a4a26">IFunctionDiscoveryProvider</a>
 

 


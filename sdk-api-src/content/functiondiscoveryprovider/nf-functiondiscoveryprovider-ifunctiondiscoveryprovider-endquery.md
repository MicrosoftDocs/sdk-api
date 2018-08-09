---
UID: NF:functiondiscoveryprovider.IFunctionDiscoveryProvider.EndQuery
title: IFunctionDiscoveryProvider::EndQuery
author: windows-sdk-content
description: Terminates a query being executed by a provider.
old-location: ncd\ifunctiondiscoveryprovider_endquery_method.htm
old-project: fundisc
ms.assetid: be19f2ac-037c-443b-b36f-68b9c9f132f8
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: EndQuery, EndQuery method, EndQuery method,IFunctionDiscoveryProvider interface, IFunctionDiscoveryProvider interface,EndQuery method, IFunctionDiscoveryProvider.EndQuery, IFunctionDiscoveryProvider::EndQuery, functiondiscoveryprovider/IFunctionDiscoveryProvider::EndQuery, ncd.ifunctiondiscoveryprovider_endquery_method
ms.prod: windows
ms.technology: windows-sdk
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
 - IFunctionDiscoveryProvider.EndQuery
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# IFunctionDiscoveryProvider::EndQuery


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Terminates a query being executed by a provider.


## -parameters






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



This method is called by Function Discovery to indicate to a provider that no further query notifications will be sent to the <a href="https://msdn.microsoft.com/1819fe08-b151-482d-8e2c-1d599fd15609">IFunctionDiscoveryNotification</a> callback interface. Implementers should try to ensure that no further query notifications are sent to Function Discovery after the call to <b>EndQuery</b> returns. If a provider implementation sends a notification after <b>EndQuery</b>  returns, Function Discovery returns an error to the provider and the notification is not forwarded to the client. 

<b>EndQuery</b> is only called when a client passed an <a href="https://msdn.microsoft.com/1819fe08-b151-482d-8e2c-1d599fd15609">IFunctionDiscoveryNotification</a> interface passed to the provider's <a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a> method.

Any data structures associated with the query can be deleted in the implementation of <b>EndQuery</b>. Any private context memory allocated by the <a href="https://msdn.microsoft.com/library/windows/hardware/hh406403">Query</a> method should also be deleted.

Note that <a href="https://msdn.microsoft.com/library/windows/hardware/hh406403">Query</a> can be invoked again once <b>EndQuery</b> has returned.




## -see-also




<a href="https://msdn.microsoft.com/e0019d0d-1495-4a0e-a7d9-7772046a4a26">IFunctionDiscoveryProvider</a>
 

 


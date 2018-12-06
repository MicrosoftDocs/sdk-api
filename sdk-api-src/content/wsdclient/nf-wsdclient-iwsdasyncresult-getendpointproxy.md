---
UID: NF:wsdclient.IWSDAsyncResult.GetEndpointProxy
title: IWSDAsyncResult::GetEndpointProxy
author: windows-sdk-content
description: Retrieves the endpoint proxy for the asynchronous operation.
old-location: ncd\iwsdasyncresult_getendpointproxy.htm
tech.root: wsdapi
ms.assetid: f2b1f43a-e86c-4ec9-a39f-9c5050f3e3c3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetEndpointProxy, GetEndpointProxy method, GetEndpointProxy method,IWSDAsyncResult interface, IWSDAsyncResult interface,GetEndpointProxy method, IWSDAsyncResult.GetEndpointProxy, IWSDAsyncResult::GetEndpointProxy, ncd.iwsdasyncresult_getendpointproxy, wsdclient/IWSDAsyncResult::GetEndpointProxy
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wsdclient.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wsdclient.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wsdapi.dll
api_name:
 - IWSDAsyncResult.GetEndpointProxy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSDAsyncResult::GetEndpointProxy


## -description


Retrieves the endpoint proxy for the asynchronous operation.


## -parameters




### -param ppEndpoint [out]

An <a href="https://msdn.microsoft.com/58ca085f-8939-413c-8fd3-4d867b1cf490">IWSDEndpointProxy</a> interface that implements an endpoint proxy.


## -returns



This method can return one of these values.


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
Method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>ppEndpoint</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/49c5ad02-f24b-4ef9-b943-483728c0bbcd">IWSDAsyncResult</a>
 

 


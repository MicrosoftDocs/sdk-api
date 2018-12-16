---
UID: NF:wsdclient.IWSDEndpointProxy.SendTwoWayRequest
title: IWSDEndpointProxy::SendTwoWayRequest
author: windows-sdk-content
description: Sends a two-way request message using a synchronous call pattern.
old-location: ncd\iwsdendpointproxy_sendtwowayrequest.htm
tech.root: wsdapi
ms.assetid: f93ddbf1-d530-4957-87ab-5718ee5f20d9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWSDEndpointProxy interface,SendTwoWayRequest method, IWSDEndpointProxy.SendTwoWayRequest, IWSDEndpointProxy::SendTwoWayRequest, SendTwoWayRequest, SendTwoWayRequest method, SendTwoWayRequest method,IWSDEndpointProxy interface, ncd.iwsdendpointproxy_sendtwowayrequest, wsdclient/IWSDEndpointProxy::SendTwoWayRequest
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
req.idl: WsdClient.idl
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
 - Wsdapi.dll
api_name:
 - IWSDEndpointProxy.SendTwoWayRequest
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSDEndpointProxy::SendTwoWayRequest


## -description


Sends a two-way request message using a synchronous call pattern.


## -parameters




### -param pBody [in]

The body of the message.


### -param pOperation [in]

Reference to a <a href="https://msdn.microsoft.com/fcd4895d-5357-4b73-90b9-e506e3d7f16e">WSD_OPERATION</a> structure that specifies the operation to perform.


### -param pResponseContext [in, optional]

 Reference to a <a href="https://msdn.microsoft.com/591cf076-f55f-4e78-aa5e-94ea8db3d102">WSD_SYNCHRONOUS_RESPONSE_CONTEXT</a> structure or other context structure that specifies the context for handling the response to the request. 



## -returns



Possible return values include, but are not limited to, the following:

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
<i>pOperation</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



This method is normally only called by generated proxy code.




<a href="https://msdn.microsoft.com/591cf076-f55f-4e78-aa5e-94ea8db3d102">WSD_SYNCHRONOUS_RESPONSE_CONTEXT</a> is used for the <i>responseContext</i> value when a synchronous call pattern is used. 




## -see-also




<a href="https://msdn.microsoft.com/58ca085f-8939-413c-8fd3-4d867b1cf490">IWSDEndpointProxy</a>
 

 


---
UID: NF:wsdclient.IWSDEndpointProxy.SendOneWayRequest
title: IWSDEndpointProxy::SendOneWayRequest
author: windows-sdk-content
description: Sends a one-way request message.
old-location: ncd\iwsdendpointproxy_sendonewayrequest.htm
tech.root: WsdApi
ms.assetid: e610c68f-1fce-42fa-8527-8ca2d9267c90
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IWSDEndpointProxy interface,SendOneWayRequest method, IWSDEndpointProxy.SendOneWayRequest, IWSDEndpointProxy::SendOneWayRequest, SendOneWayRequest, SendOneWayRequest method, SendOneWayRequest method,IWSDEndpointProxy interface, ncd.iwsdendpointproxy_sendonewayrequest, wsdclient/IWSDEndpointProxy::SendOneWayRequest
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
 - IWSDEndpointProxy.SendOneWayRequest
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSDEndpointProxy::SendOneWayRequest


## -description


Sends a one-way request message.


## -parameters




### -param pBody [in]

 The body of the message.


### -param pOperation [in]

Reference to a <a href="https://msdn.microsoft.com/fcd4895d-5357-4b73-90b9-e506e3d7f16e">WSD_OPERATION</a> structure that specifies the operation to perform.


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




## -see-also




<a href="https://msdn.microsoft.com/58ca085f-8939-413c-8fd3-4d867b1cf490">IWSDEndpointProxy</a>
 

 


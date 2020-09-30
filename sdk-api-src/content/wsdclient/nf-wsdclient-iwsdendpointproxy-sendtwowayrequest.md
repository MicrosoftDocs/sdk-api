---
UID: NF:wsdclient.IWSDEndpointProxy.SendTwoWayRequest
title: IWSDEndpointProxy::SendTwoWayRequest (wsdclient.h)
description: Sends a two-way request message using a synchronous call pattern.
helpviewer_keywords: ["IWSDEndpointProxy interface","SendTwoWayRequest method","IWSDEndpointProxy.SendTwoWayRequest","IWSDEndpointProxy::SendTwoWayRequest","SendTwoWayRequest","SendTwoWayRequest method","SendTwoWayRequest method","IWSDEndpointProxy interface","ncd.iwsdendpointproxy_sendtwowayrequest","wsdclient/IWSDEndpointProxy::SendTwoWayRequest"]
old-location: ncd\iwsdendpointproxy_sendtwowayrequest.htm
tech.root: ncd
ms.assetid: f93ddbf1-d530-4957-87ab-5718ee5f20d9
ms.date: 12/05/2018
ms.keywords: IWSDEndpointProxy interface,SendTwoWayRequest method, IWSDEndpointProxy.SendTwoWayRequest, IWSDEndpointProxy::SendTwoWayRequest, SendTwoWayRequest, SendTwoWayRequest method, SendTwoWayRequest method,IWSDEndpointProxy interface, ncd.iwsdendpointproxy_sendtwowayrequest, wsdclient/IWSDEndpointProxy::SendTwoWayRequest
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWSDEndpointProxy::SendTwoWayRequest
 - wsdclient/IWSDEndpointProxy::SendTwoWayRequest
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDEndpointProxy.SendTwoWayRequest
---

# IWSDEndpointProxy::SendTwoWayRequest


## -description

Sends a two-way request message using a synchronous call pattern.

## -parameters

### -param pBody [in]

The body of the message.

### -param pOperation [in]

Reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_operation">WSD_OPERATION</a> structure that specifies the operation to perform.

### -param pResponseContext [in, optional]

 Reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_synchronous_response_context">WSD_SYNCHRONOUS_RESPONSE_CONTEXT</a> structure or other context structure that specifies the context for handling the response to the request.

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




<a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_synchronous_response_context">WSD_SYNCHRONOUS_RESPONSE_CONTEXT</a> is used for the <i>responseContext</i> value when a synchronous call pattern is used.

## -see-also

<a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdendpointproxy">IWSDEndpointProxy</a>
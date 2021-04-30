---
UID: NF:wsdclient.IWSDEndpointProxy.SendOneWayRequest
title: IWSDEndpointProxy::SendOneWayRequest (wsdclient.h)
description: Sends a one-way request message.
helpviewer_keywords: ["IWSDEndpointProxy interface","SendOneWayRequest method","IWSDEndpointProxy.SendOneWayRequest","IWSDEndpointProxy::SendOneWayRequest","SendOneWayRequest","SendOneWayRequest method","SendOneWayRequest method","IWSDEndpointProxy interface","ncd.iwsdendpointproxy_sendonewayrequest","wsdclient/IWSDEndpointProxy::SendOneWayRequest"]
old-location: ncd\iwsdendpointproxy_sendonewayrequest.htm
tech.root: ncd
ms.assetid: e610c68f-1fce-42fa-8527-8ca2d9267c90
ms.date: 12/05/2018
ms.keywords: IWSDEndpointProxy interface,SendOneWayRequest method, IWSDEndpointProxy.SendOneWayRequest, IWSDEndpointProxy::SendOneWayRequest, SendOneWayRequest, SendOneWayRequest method, SendOneWayRequest method,IWSDEndpointProxy interface, ncd.iwsdendpointproxy_sendonewayrequest, wsdclient/IWSDEndpointProxy::SendOneWayRequest
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
 - IWSDEndpointProxy::SendOneWayRequest
 - wsdclient/IWSDEndpointProxy::SendOneWayRequest
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
 - IWSDEndpointProxy.SendOneWayRequest
---

# IWSDEndpointProxy::SendOneWayRequest


## -description

Sends a one-way request message.

## -parameters

### -param pBody [in]

 The body of the message.

### -param pOperation [in]

Reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_operation">WSD_OPERATION</a> structure that specifies the operation to perform.

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

<a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdendpointproxy">IWSDEndpointProxy</a>
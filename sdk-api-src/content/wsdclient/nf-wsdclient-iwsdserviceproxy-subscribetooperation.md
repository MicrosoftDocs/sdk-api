---
UID: NF:wsdclient.IWSDServiceProxy.SubscribeToOperation
title: IWSDServiceProxy::SubscribeToOperation (wsdclient.h)
description: Subscribes to a notification or solicit/response event.
helpviewer_keywords: ["IWSDServiceProxy interface","SubscribeToOperation method","IWSDServiceProxy.SubscribeToOperation","IWSDServiceProxy::SubscribeToOperation","SubscribeToOperation","SubscribeToOperation method","SubscribeToOperation method","IWSDServiceProxy interface","ncd.iwsdserviceproxy_subscribetooperation_method","wsdclient/IWSDServiceProxy::SubscribeToOperation"]
old-location: ncd\iwsdserviceproxy_subscribetooperation_method.htm
tech.root: ncd
ms.assetid: d3294bd7-f3df-4571-92f6-eb6bc57240fb
ms.date: 12/05/2018
ms.keywords: IWSDServiceProxy interface,SubscribeToOperation method, IWSDServiceProxy.SubscribeToOperation, IWSDServiceProxy::SubscribeToOperation, SubscribeToOperation, SubscribeToOperation method, SubscribeToOperation method,IWSDServiceProxy interface, ncd.iwsdserviceproxy_subscribetooperation_method, wsdclient/IWSDServiceProxy::SubscribeToOperation
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
 - IWSDServiceProxy::SubscribeToOperation
 - wsdclient/IWSDServiceProxy::SubscribeToOperation
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
 - IWSDServiceProxy.SubscribeToOperation
---

# IWSDServiceProxy::SubscribeToOperation


## -description

Subscribes to a notification or solicit/response event.

## -parameters

### -param pOperation [in]

 Reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_operation">WSD_OPERATION</a> structure that specifies the operation to subscribe to.

### -param pUnknown [in]

 
Anonymous data passed to a client eventing callback function. This data is used to associate a client object with the subscription.

### -param pAny [in]

Extensible data to be added to the body of the subscription request. You can use the IWSDXML* interfaces to build the data. For details, see <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_element">WSDXML_ELEMENT</a>.

### -param ppAny [out]

Extensible data that the remote device can add to the subscription response. This allows services to provide additional customization of event subscriptions. When done, call  <a href="/windows/desktop/api/wsdutil/nf-wsdutil-wsdfreelinkedmemory">WSDFreeLinkedMemory</a> to free the memory. For details, see <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_element">WSDXML_ELEMENT</a>. Do not release this object.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The proxy has already subscribed to the operation specified by <i>pOperation</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed.

</td>
</tr>
</table>

## -remarks

This method is normally only called by generated proxy code.

## -see-also

<a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdserviceproxy">IWSDServiceProxy</a>
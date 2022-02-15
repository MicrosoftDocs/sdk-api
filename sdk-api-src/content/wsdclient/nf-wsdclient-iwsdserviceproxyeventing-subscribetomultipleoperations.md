---
UID: NF:wsdclient.IWSDServiceProxyEventing.SubscribeToMultipleOperations
title: IWSDServiceProxyEventing::SubscribeToMultipleOperations (wsdclient.h)
description: Subscribes to a collection of notifications or solicit/response events.
helpviewer_keywords: ["IWSDServiceProxyEventing interface","SubscribeToMultipleOperations method","IWSDServiceProxyEventing.SubscribeToMultipleOperations","IWSDServiceProxyEventing::SubscribeToMultipleOperations","SubscribeToMultipleOperations","SubscribeToMultipleOperations method","SubscribeToMultipleOperations method","IWSDServiceProxyEventing interface","ncd.iwsdserviceproxyeventing_subscribetomultipleoperations","wsdclient/IWSDServiceProxyEventing::SubscribeToMultipleOperations"]
old-location: ncd\iwsdserviceproxyeventing_subscribetomultipleoperations.htm
tech.root: ncd
ms.assetid: 0df5b429-5b6e-4cef-af05-7f615c93aa0f
ms.date: 12/05/2018
ms.keywords: IWSDServiceProxyEventing interface,SubscribeToMultipleOperations method, IWSDServiceProxyEventing.SubscribeToMultipleOperations, IWSDServiceProxyEventing::SubscribeToMultipleOperations, SubscribeToMultipleOperations, SubscribeToMultipleOperations method, SubscribeToMultipleOperations method,IWSDServiceProxyEventing interface, ncd.iwsdserviceproxyeventing_subscribetomultipleoperations, wsdclient/IWSDServiceProxyEventing::SubscribeToMultipleOperations
req.header: wsdclient.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWSDServiceProxyEventing::SubscribeToMultipleOperations
 - wsdclient/IWSDServiceProxyEventing::SubscribeToMultipleOperations
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wsdapi.dll
api_name:
 - IWSDServiceProxyEventing.SubscribeToMultipleOperations
---

# IWSDServiceProxyEventing::SubscribeToMultipleOperations


## -description

Subscribes to a collection of notifications or solicit/response events.

## -parameters

### -param pOperations [in]

Pointer to an array of references to <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_operation">WSD_OPERATION</a> structures that specify the operations of whiCh to subscribe.

### -param dwOperationCount [in]

The number of elements in the array in <i>pOperations</i>.

### -param pUnknown [in]

Anonymous data passed to a client eventing callback function. This data is used to associate a client object with the subscription.

### -param pExpires [in]

Pointer to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_eventing_expires">WSD_EVENTING_EXPIRES</a> structure that specifies requested duration for the subscription.

### -param pAny [in]

Pointer to extensible data to be added to the body of the request.  This parameter is optional.

### -param ppExpires [out]

Pointer to a pointer to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_eventing_expires">WSD_EVENTING_EXPIRES</a> structure that specfies the duration of the subscription.  Upon completion, call  <a href="/windows/desktop/api/wsdutil/nf-wsdutil-wsdfreelinkedmemory">WSDFreeLinkedMemory</a> to free the memory.   This parameter is optional.

### -param ppAny [out]

Extensible data that the remote device can add to the subscription response. This allows services to provide additional customization of event subscriptions. When done, call  <a href="/windows/desktop/api/wsdutil/nf-wsdutil-wsdfreelinkedmemory">WSDFreeLinkedMemory</a> to free the memory. For details, see <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_element">WSDXML_ELEMENT</a>.   This parameter is optional.

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

This method is designed to be exclusively called by generated proxy code.

The method is synchronous and will return when the requests have completed or the expiration criteria have been satisfied.

## -see-also

<a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdserviceproxyeventing">IWSDServiceProxyEventing</a>
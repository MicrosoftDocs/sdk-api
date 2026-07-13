---
UID: NF:wsdclient.IWSDServiceProxyEventing.EndSubscribeToMultipleOperations
title: IWSDServiceProxyEventing::EndSubscribeToMultipleOperations (wsdclient.h)
description: Completes an asynchronous operation that subscribes to a collection of notifications or solicit/response events.
helpviewer_keywords: ["EndSubscribeToMultipleOperations","EndSubscribeToMultipleOperations method","EndSubscribeToMultipleOperations method","IWSDServiceProxyEventing interface","IWSDServiceProxyEventing interface","EndSubscribeToMultipleOperations method","IWSDServiceProxyEventing.EndSubscribeToMultipleOperations","IWSDServiceProxyEventing::EndSubscribeToMultipleOperations","ncd.iwsdserviceproxyeventing_endsubscribetomultipleoperations","wsdclient/IWSDServiceProxyEventing::EndSubscribeToMultipleOperations"]
old-location: ncd\iwsdserviceproxyeventing_endsubscribetomultipleoperations.htm
tech.root: ncd
ms.assetid: 2e3cdb10-fde9-4936-9a7d-61404a754faa
ms.date: 12/05/2018
ms.keywords: EndSubscribeToMultipleOperations, EndSubscribeToMultipleOperations method, EndSubscribeToMultipleOperations method,IWSDServiceProxyEventing interface, IWSDServiceProxyEventing interface,EndSubscribeToMultipleOperations method, IWSDServiceProxyEventing.EndSubscribeToMultipleOperations, IWSDServiceProxyEventing::EndSubscribeToMultipleOperations, ncd.iwsdserviceproxyeventing_endsubscribetomultipleoperations, wsdclient/IWSDServiceProxyEventing::EndSubscribeToMultipleOperations
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
 - IWSDServiceProxyEventing::EndSubscribeToMultipleOperations
 - wsdclient/IWSDServiceProxyEventing::EndSubscribeToMultipleOperations
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
 - IWSDServiceProxyEventing.EndSubscribeToMultipleOperations
---

# IWSDServiceProxyEventing::EndSubscribeToMultipleOperations


## -description

Completes an asynchronous operation that subscribes to a collection of notifications or solicit/response events.

## -parameters

### -param pOperations [in]

Pointer to an array of references to <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_operation">WSD_OPERATION</a> structures that specify the subscribed operations.

### -param dwOperationCount [in]

The number of elements in the array in <i>pOperations</i>.

### -param pResult [out]

Pointer to an <a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdasyncresult">IWSDAsyncResult</a> interface that represents the result of the requests upon completion.

### -param ppExpires [out]

Pointer to a pointer to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_eventing_expires">WSD_EVENTING_EXPIRES</a> structure that specfies the duration of the subscription.  Upon completion, call  <a href="/windows/desktop/api/wsdutil/nf-wsdutil-wsdfreelinkedmemory">WSDFreeLinkedMemory</a> to free the memory.  This parameter is optional.

### -param ppAny [out]

Extensible data that the remote device can add to the subscription response. This allows services to provide additional customization of event subscriptions. When done, call  <a href="/windows/desktop/api/wsdutil/nf-wsdutil-wsdfreelinkedmemory">WSDFreeLinkedMemory</a> to free the memory. For details, see <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_element">WSDXML_ELEMENT</a>.  This parameter is optional.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is designed to be exclusively called by generated proxy code.

The method is used to obtain the results from a previous asynchronous <a href="/windows/desktop/api/wsdclient/nf-wsdclient-iwsdserviceproxyeventing-beginsubscribetomultipleoperations">BeginSubscribeToMultipleOperations</a> call.

## -see-also

<a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdserviceproxyeventing">IWSDServiceProxyEventing</a>
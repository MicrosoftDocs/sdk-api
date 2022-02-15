---
UID: NF:wsdclient.IWSDServiceProxyEventing.BeginSubscribeToMultipleOperations
title: IWSDServiceProxyEventing::BeginSubscribeToMultipleOperations (wsdclient.h)
description: Initializes an asynchronous operation that subscribes to a collection of notifications or solicit/response events.
helpviewer_keywords: ["BeginSubscribeToMultipleOperations","BeginSubscribeToMultipleOperations method","BeginSubscribeToMultipleOperations method","IWSDServiceProxyEventing interface","IWSDServiceProxyEventing interface","BeginSubscribeToMultipleOperations method","IWSDServiceProxyEventing.BeginSubscribeToMultipleOperations","IWSDServiceProxyEventing::BeginSubscribeToMultipleOperations","ncd.iwsdserviceproxyeventing_beginsubscribetomultipleoperations","wsdclient/IWSDServiceProxyEventing::BeginSubscribeToMultipleOperations"]
old-location: ncd\iwsdserviceproxyeventing_beginsubscribetomultipleoperations.htm
tech.root: ncd
ms.assetid: 54c6ac58-4272-45ad-80cc-2114ba6f466e
ms.date: 12/05/2018
ms.keywords: BeginSubscribeToMultipleOperations, BeginSubscribeToMultipleOperations method, BeginSubscribeToMultipleOperations method,IWSDServiceProxyEventing interface, IWSDServiceProxyEventing interface,BeginSubscribeToMultipleOperations method, IWSDServiceProxyEventing.BeginSubscribeToMultipleOperations, IWSDServiceProxyEventing::BeginSubscribeToMultipleOperations, ncd.iwsdserviceproxyeventing_beginsubscribetomultipleoperations, wsdclient/IWSDServiceProxyEventing::BeginSubscribeToMultipleOperations
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
 - IWSDServiceProxyEventing::BeginSubscribeToMultipleOperations
 - wsdclient/IWSDServiceProxyEventing::BeginSubscribeToMultipleOperations
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
 - IWSDServiceProxyEventing.BeginSubscribeToMultipleOperations
---

# IWSDServiceProxyEventing::BeginSubscribeToMultipleOperations


## -description

Initializes an asynchronous operation that subscribes to a collection of notifications or solicit/response events.

## -parameters

### -param pOperations [in]

Pointer to an array of references to <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_operation">WSD_OPERATION</a> structures that specify the operations of which to subscribe.

### -param dwOperationCount [in]

The number of elements in the array in <i>pOperations</i>.

### -param pUnknown [in]

Anonymous data passed to a client eventing callback function. This data is used to associate a client object with the subscription.

### -param pExpires [in]

Pointer to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_eventing_expires">WSD_EVENTING_EXPIRES</a> structure that specifies the requested duration for the subscription.

### -param pAny [in]

Pointer to extensible data to be added to the body of the request.  This parameter is optional.

### -param pAsyncState [in]

Anonymous data passed to <i>pAsyncCallback</i> when the callback is called.  This data is used to associate a client object with the pending operation.  This parameter is optional.

### -param pAsyncCallback [in]

Reference to an <a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdasynccallback">IWSDAsyncCallback</a> object that performs the message callback status notifications.  This parameter is optional.

### -param ppResult [out]

Pointer to a pointer to an <a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdasyncresult">IWSDAsyncResult</a> interface that will represent the result of the requests upon completion.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is designed to be exclusively called by generated proxy code.

The method is asynchronous and will return immediately.    The caller should subsequently call <a href="/windows/desktop/api/wsdclient/nf-wsdclient-iwsdserviceproxyeventing-endsubscribetomultipleoperations">EndSubscribeToMultipleOperations</a>.

## -see-also

<a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdserviceproxyeventing">IWSDServiceProxyEventing</a>
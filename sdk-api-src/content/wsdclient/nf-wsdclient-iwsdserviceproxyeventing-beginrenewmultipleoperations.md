---
UID: NF:wsdclient.IWSDServiceProxyEventing.BeginRenewMultipleOperations
title: IWSDServiceProxyEventing::BeginRenewMultipleOperations (wsdclient.h)
description: Initializes an asynchronous operation that renews a collection of existing notification subscriptions by submitting a new duration.
helpviewer_keywords: ["BeginRenewMultipleOperations","BeginRenewMultipleOperations method","BeginRenewMultipleOperations method","IWSDServiceProxyEventing interface","IWSDServiceProxyEventing interface","BeginRenewMultipleOperations method","IWSDServiceProxyEventing.BeginRenewMultipleOperations","IWSDServiceProxyEventing::BeginRenewMultipleOperations","ncd.iwsdserviceproxyeventing_beginrenewmultipleoperations","wsdclient/IWSDServiceProxyEventing::BeginRenewMultipleOperations"]
old-location: ncd\iwsdserviceproxyeventing_beginrenewmultipleoperations.htm
tech.root: ncd
ms.assetid: ac93a29a-789f-4aa0-b804-b4d0a5b89ee2
ms.date: 12/05/2018
ms.keywords: BeginRenewMultipleOperations, BeginRenewMultipleOperations method, BeginRenewMultipleOperations method,IWSDServiceProxyEventing interface, IWSDServiceProxyEventing interface,BeginRenewMultipleOperations method, IWSDServiceProxyEventing.BeginRenewMultipleOperations, IWSDServiceProxyEventing::BeginRenewMultipleOperations, ncd.iwsdserviceproxyeventing_beginrenewmultipleoperations, wsdclient/IWSDServiceProxyEventing::BeginRenewMultipleOperations
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
 - IWSDServiceProxyEventing::BeginRenewMultipleOperations
 - wsdclient/IWSDServiceProxyEventing::BeginRenewMultipleOperations
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
 - IWSDServiceProxyEventing.BeginRenewMultipleOperations
---

# IWSDServiceProxyEventing::BeginRenewMultipleOperations


## -description

Initializes an asynchronous operation that renews a collection of existing notification subscriptions by submitting a new duration.

## -parameters

### -param pOperations [in]

Pointer to an array of references to <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_operation">WSD_OPERATION</a> structures that specify the operation subscriptions to renew.

### -param dwOperationCount [in]

The number of elements in the array in <i>pOperations</i>.

### -param pExpires [in]

Pointer to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_eventing_expires">WSD_EVENTING_EXPIRES</a> structure that specifies requested duration for the subscription.

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

## -see-also

<a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdserviceproxyeventing">IWSDServiceProxyEventing</a>
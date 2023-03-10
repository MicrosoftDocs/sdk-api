---
UID: NF:wsdclient.IWSDServiceProxyEventing.BeginGetStatusForMultipleOperations
title: IWSDServiceProxyEventing::BeginGetStatusForMultipleOperations (wsdclient.h)
description: Begins an asynchronous operation that retrieves the current status.
helpviewer_keywords: ["BeginGetStatusForMultipleOperations","BeginGetStatusForMultipleOperations method","BeginGetStatusForMultipleOperations method","IWSDServiceProxyEventing interface","IWSDServiceProxyEventing interface","BeginGetStatusForMultipleOperations method","IWSDServiceProxyEventing.BeginGetStatusForMultipleOperations","IWSDServiceProxyEventing::BeginGetStatusForMultipleOperations","ncd.iwsdserviceproxyeventing_begingetstatusformultipleoperations","wsdclient/IWSDServiceProxyEventing::BeginGetStatusForMultipleOperations"]
old-location: ncd\iwsdserviceproxyeventing_begingetstatusformultipleoperations.htm
tech.root: ncd
ms.assetid: cf42f680-f19c-4ee3-824d-dc892608d4d2
ms.date: 12/05/2018
ms.keywords: BeginGetStatusForMultipleOperations, BeginGetStatusForMultipleOperations method, BeginGetStatusForMultipleOperations method,IWSDServiceProxyEventing interface, IWSDServiceProxyEventing interface,BeginGetStatusForMultipleOperations method, IWSDServiceProxyEventing.BeginGetStatusForMultipleOperations, IWSDServiceProxyEventing::BeginGetStatusForMultipleOperations, ncd.iwsdserviceproxyeventing_begingetstatusformultipleoperations, wsdclient/IWSDServiceProxyEventing::BeginGetStatusForMultipleOperations
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
 - IWSDServiceProxyEventing::BeginGetStatusForMultipleOperations
 - wsdclient/IWSDServiceProxyEventing::BeginGetStatusForMultipleOperations
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
 - IWSDServiceProxyEventing.BeginGetStatusForMultipleOperations
---

# IWSDServiceProxyEventing::BeginGetStatusForMultipleOperations


## -description

Begins an asynchronous operation that retrieves the current status  for a collection of event subscriptions.

## -parameters

### -param pOperations [in]

Pointer to an array of references to <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_operation">WSD_OPERATION</a> structures that specify the operation subscriptions to get status on.

### -param dwOperationCount [in]

The number of elements in the array in <i>pOperations</i>.

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
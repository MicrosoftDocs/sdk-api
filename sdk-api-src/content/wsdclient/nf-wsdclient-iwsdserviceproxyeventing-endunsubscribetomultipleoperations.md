---
UID: NF:wsdclient.IWSDServiceProxyEventing.EndUnsubscribeToMultipleOperations
title: IWSDServiceProxyEventing::EndUnsubscribeToMultipleOperations (wsdclient.h)
description: Completes an asynchronous cancellation request for a subscription to a collection of notifications or solicit/response events.
helpviewer_keywords: ["EndUnsubscribeToMultipleOperations","EndUnsubscribeToMultipleOperations method","EndUnsubscribeToMultipleOperations method","IWSDServiceProxyEventing interface","IWSDServiceProxyEventing interface","EndUnsubscribeToMultipleOperations method","IWSDServiceProxyEventing.EndUnsubscribeToMultipleOperations","IWSDServiceProxyEventing::EndUnsubscribeToMultipleOperations","ncd.iwsdserviceproxyeventing_endunsubscribetomultipleoperations","wsdclient/IWSDServiceProxyEventing::EndUnsubscribeToMultipleOperations"]
old-location: ncd\iwsdserviceproxyeventing_endunsubscribetomultipleoperations.htm
tech.root: ncd
ms.assetid: 62f42441-11b0-46ce-9a4e-03b34d8b4c9b
ms.date: 12/05/2018
ms.keywords: EndUnsubscribeToMultipleOperations, EndUnsubscribeToMultipleOperations method, EndUnsubscribeToMultipleOperations method,IWSDServiceProxyEventing interface, IWSDServiceProxyEventing interface,EndUnsubscribeToMultipleOperations method, IWSDServiceProxyEventing.EndUnsubscribeToMultipleOperations, IWSDServiceProxyEventing::EndUnsubscribeToMultipleOperations, ncd.iwsdserviceproxyeventing_endunsubscribetomultipleoperations, wsdclient/IWSDServiceProxyEventing::EndUnsubscribeToMultipleOperations
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
 - IWSDServiceProxyEventing::EndUnsubscribeToMultipleOperations
 - wsdclient/IWSDServiceProxyEventing::EndUnsubscribeToMultipleOperations
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
 - IWSDServiceProxyEventing.EndUnsubscribeToMultipleOperations
---

# IWSDServiceProxyEventing::EndUnsubscribeToMultipleOperations


## -description

Completes an  asynchronous cancellation request for a subscription to  a collection of notifications or solicit/response events.

## -parameters

### -param pOperations [in]

Pointer to an array of references to <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_operation">WSD_OPERATION</a> structures that specifies the operations from which to unsubscribe.

### -param dwOperationCount [in]

The number of elements in the array in <i>pOperations</i>.

### -param pResult [out]

Pointer to an <a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdasyncresult">IWSDAsyncResult</a> interface that will represent the result of the requests upon completion.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdserviceproxyeventing">IWSDServiceProxyEventing</a>
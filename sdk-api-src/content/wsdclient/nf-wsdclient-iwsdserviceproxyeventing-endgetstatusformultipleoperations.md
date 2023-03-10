---
UID: NF:wsdclient.IWSDServiceProxyEventing.EndGetStatusForMultipleOperations
title: IWSDServiceProxyEventing::EndGetStatusForMultipleOperations (wsdclient.h)
description: Completes an asynchronous operation that retrieves the current status.
helpviewer_keywords: ["EndGetStatusForMultipleOperations","EndGetStatusForMultipleOperations method","EndGetStatusForMultipleOperations method","IWSDServiceProxyEventing interface","IWSDServiceProxyEventing interface","EndGetStatusForMultipleOperations method","IWSDServiceProxyEventing.EndGetStatusForMultipleOperations","IWSDServiceProxyEventing::EndGetStatusForMultipleOperations","ncd.iwsdserviceproxyeventing_endgetstatusformultipleoperations","wsdclient/IWSDServiceProxyEventing::EndGetStatusForMultipleOperations"]
old-location: ncd\iwsdserviceproxyeventing_endgetstatusformultipleoperations.htm
tech.root: ncd
ms.assetid: 0918ef4f-29ae-4c74-9b7d-0e7adb514c7b
ms.date: 12/05/2018
ms.keywords: EndGetStatusForMultipleOperations, EndGetStatusForMultipleOperations method, EndGetStatusForMultipleOperations method,IWSDServiceProxyEventing interface, IWSDServiceProxyEventing interface,EndGetStatusForMultipleOperations method, IWSDServiceProxyEventing.EndGetStatusForMultipleOperations, IWSDServiceProxyEventing::EndGetStatusForMultipleOperations, ncd.iwsdserviceproxyeventing_endgetstatusformultipleoperations, wsdclient/IWSDServiceProxyEventing::EndGetStatusForMultipleOperations
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
 - IWSDServiceProxyEventing::EndGetStatusForMultipleOperations
 - wsdclient/IWSDServiceProxyEventing::EndGetStatusForMultipleOperations
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
 - IWSDServiceProxyEventing.EndGetStatusForMultipleOperations
---

# IWSDServiceProxyEventing::EndGetStatusForMultipleOperations


## -description

Completes an asynchronous operation that retrieves the current status  for a collection of event subscriptions.

## -parameters

### -param pOperations [in]

Pointer to an array of references to <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_operation">WSD_OPERATION</a> structures that specify the operation subscriptions to get status on.

### -param dwOperationCount [in]

The number of elements in the array in <i>pOperations</i>.

### -param pResult [in]

Pointer to an <a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdasyncresult">IWSDAsyncResult</a> interface that represents the result of the requests upon completion.

### -param ppExpires [out]

Pointer to a pointer to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_eventing_expires">WSD_EVENTING_EXPIRES</a> structure that specfies the duration of the subscription.  Upon completion, call  <a href="/windows/desktop/api/wsdutil/nf-wsdutil-wsdfreelinkedmemory">WSDFreeLinkedMemory</a> to free the memory.   This parameter is optional.

### -param ppAny [out]

Extensible data that the remote device can add to the subscription response. This allows services to provide additional customization of getstatu requests. When done, call  <a href="/windows/desktop/api/wsdutil/nf-wsdutil-wsdfreelinkedmemory">WSDFreeLinkedMemory</a> to free the memory. For details, see <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_element">WSDXML_ELEMENT</a>.  This parameter is optional.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdserviceproxyeventing">IWSDServiceProxyEventing</a>
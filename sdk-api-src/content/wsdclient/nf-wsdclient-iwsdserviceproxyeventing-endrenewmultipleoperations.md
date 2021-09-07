---
UID: NF:wsdclient.IWSDServiceProxyEventing.EndRenewMultipleOperations
title: IWSDServiceProxyEventing::EndRenewMultipleOperations (wsdclient.h)
description: Completes an asynchronous operation that renews a collection of existing notification subscriptions by submitting a new duration.
helpviewer_keywords: ["EndRenewMultipleOperations","EndRenewMultipleOperations method","EndRenewMultipleOperations method","IWSDServiceProxyEventing interface","IWSDServiceProxyEventing interface","EndRenewMultipleOperations method","IWSDServiceProxyEventing.EndRenewMultipleOperations","IWSDServiceProxyEventing::EndRenewMultipleOperations","ncd.iwsdserviceproxyeventing_endrenewmultipleoperations","wsdclient/IWSDServiceProxyEventing::EndRenewMultipleOperations"]
old-location: ncd\iwsdserviceproxyeventing_endrenewmultipleoperations.htm
tech.root: ncd
ms.assetid: fb5be204-a775-4abb-af5b-9a829b69fa14
ms.date: 12/05/2018
ms.keywords: EndRenewMultipleOperations, EndRenewMultipleOperations method, EndRenewMultipleOperations method,IWSDServiceProxyEventing interface, IWSDServiceProxyEventing interface,EndRenewMultipleOperations method, IWSDServiceProxyEventing.EndRenewMultipleOperations, IWSDServiceProxyEventing::EndRenewMultipleOperations, ncd.iwsdserviceproxyeventing_endrenewmultipleoperations, wsdclient/IWSDServiceProxyEventing::EndRenewMultipleOperations
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
 - IWSDServiceProxyEventing::EndRenewMultipleOperations
 - wsdclient/IWSDServiceProxyEventing::EndRenewMultipleOperations
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
 - IWSDServiceProxyEventing.EndRenewMultipleOperations
---

# IWSDServiceProxyEventing::EndRenewMultipleOperations


## -description

Completes an asynchronous operation that renews a collection of existing notification subscriptions by submitting a new duration.

## -parameters

### -param pOperations [in]

Pointer to an array of references to <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_operation">WSD_OPERATION</a> structures that specify the operation subscriptions to renew.

### -param dwOperationCount [in]

The number of elements in the array in <i>pOperations</i>.

### -param pResult [in]

Pointer to an <a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdasyncresult">IWSDAsyncResult</a> interface that represents the result of the requests upon completion.

### -param ppExpires [out]

Pointer to a pointer to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_eventing_expires">WSD_EVENTING_EXPIRES</a> structure that specfies the duration of the subscription that was just renewed.  Upon completion, call  <a href="/windows/desktop/api/wsdutil/nf-wsdutil-wsdfreelinkedmemory">WSDFreeLinkedMemory</a> to free the memory.  This parameter is optional.

### -param ppAny [out]

Extensible data that the remote device can add to the subscription response. This allows services to provide additional customization of event subscriptions. When done, call  <a href="/windows/desktop/api/wsdutil/nf-wsdutil-wsdfreelinkedmemory">WSDFreeLinkedMemory</a> to free the memory. For details, see <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_element">WSDXML_ELEMENT</a>.  This parameter is optional.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdserviceproxyeventing">IWSDServiceProxyEventing</a>
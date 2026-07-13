---
UID: NF:wsdclient.IWSDServiceProxyEventing.RenewMultipleOperations
title: IWSDServiceProxyEventing::RenewMultipleOperations (wsdclient.h)
description: Renews a collection of existing notification subscriptions by submitting a new duration.
helpviewer_keywords: ["IWSDServiceProxyEventing interface","RenewMultipleOperations method","IWSDServiceProxyEventing.RenewMultipleOperations","IWSDServiceProxyEventing::RenewMultipleOperations","RenewMultipleOperations","RenewMultipleOperations method","RenewMultipleOperations method","IWSDServiceProxyEventing interface","ncd.iwsdserviceproxyeventing_renewmultipleoperations","wsdclient/IWSDServiceProxyEventing::RenewMultipleOperations"]
old-location: ncd\iwsdserviceproxyeventing_renewmultipleoperations.htm
tech.root: ncd
ms.assetid: 67c5fa63-3512-4b03-afb4-9b97b26200aa
ms.date: 12/05/2018
ms.keywords: IWSDServiceProxyEventing interface,RenewMultipleOperations method, IWSDServiceProxyEventing.RenewMultipleOperations, IWSDServiceProxyEventing::RenewMultipleOperations, RenewMultipleOperations, RenewMultipleOperations method, RenewMultipleOperations method,IWSDServiceProxyEventing interface, ncd.iwsdserviceproxyeventing_renewmultipleoperations, wsdclient/IWSDServiceProxyEventing::RenewMultipleOperations
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
 - IWSDServiceProxyEventing::RenewMultipleOperations
 - wsdclient/IWSDServiceProxyEventing::RenewMultipleOperations
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
 - IWSDServiceProxyEventing.RenewMultipleOperations
---

# IWSDServiceProxyEventing::RenewMultipleOperations


## -description

Renews a collection of existing notification subscriptions by submitting a new duration.

## -parameters

### -param pOperations [in]

Pointer to an array of references to <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_operation">WSD_OPERATION</a> structures that specify the operation subscriptions to renew.

### -param dwOperationCount [in]

The number of elements in the array in <i>pOperations</i>.

### -param pExpires [in]

Pointer to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_eventing_expires">WSD_EVENTING_EXPIRES</a> structure that specifies requested duration for the subscription.

### -param pAny [in]

Pointer to extensible data to be added to the body of the request.  This parameter is optional.

### -param ppExpires [out]

Pointer to a pointer to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_eventing_expires">WSD_EVENTING_EXPIRES</a> structure that specifies the duration of the subscription that was just renewed.  Upon completion, call  <a href="/windows/desktop/api/wsdutil/nf-wsdutil-wsdfreelinkedmemory">WSDFreeLinkedMemory</a> to free the memory.  This parameter is optional.

### -param ppAny [out]

Extensible data that the remote device can add to the subscription response. This allows services to provide additional customization of renew requests. When done, call  <a href="/windows/desktop/api/wsdutil/nf-wsdutil-wsdfreelinkedmemory">WSDFreeLinkedMemory</a> to free the memory. For details, see <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_element">WSDXML_ELEMENT</a>.  This parameter is optional.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdserviceproxyeventing">IWSDServiceProxyEventing</a>
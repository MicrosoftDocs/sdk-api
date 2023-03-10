---
UID: NF:wsdclient.IWSDServiceProxyEventing.GetStatusForMultipleOperations
title: IWSDServiceProxyEventing::GetStatusForMultipleOperations (wsdclient.h)
description: Retrieves the current status.
helpviewer_keywords: ["GetStatusForMultipleOperations","GetStatusForMultipleOperations method","GetStatusForMultipleOperations method","IWSDServiceProxyEventing interface","IWSDServiceProxyEventing interface","GetStatusForMultipleOperations method","IWSDServiceProxyEventing.GetStatusForMultipleOperations","IWSDServiceProxyEventing::GetStatusForMultipleOperations","ncd.iwsdserviceproxyeventing_getstatusformultipleoperations","wsdclient/IWSDServiceProxyEventing::GetStatusForMultipleOperations"]
old-location: ncd\iwsdserviceproxyeventing_getstatusformultipleoperations.htm
tech.root: ncd
ms.assetid: ba9c6d6e-d551-4010-b3b7-9e5391de9c49
ms.date: 12/05/2018
ms.keywords: GetStatusForMultipleOperations, GetStatusForMultipleOperations method, GetStatusForMultipleOperations method,IWSDServiceProxyEventing interface, IWSDServiceProxyEventing interface,GetStatusForMultipleOperations method, IWSDServiceProxyEventing.GetStatusForMultipleOperations, IWSDServiceProxyEventing::GetStatusForMultipleOperations, ncd.iwsdserviceproxyeventing_getstatusformultipleoperations, wsdclient/IWSDServiceProxyEventing::GetStatusForMultipleOperations
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
 - IWSDServiceProxyEventing::GetStatusForMultipleOperations
 - wsdclient/IWSDServiceProxyEventing::GetStatusForMultipleOperations
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
 - IWSDServiceProxyEventing.GetStatusForMultipleOperations
---

# IWSDServiceProxyEventing::GetStatusForMultipleOperations


## -description

Retrieves the current status  for a collection of event subscriptions.

## -parameters

### -param pOperations [in]

Pointer to an array of references to <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_operation">WSD_OPERATION</a> structures that specify the operation subscriptions to get status on.

### -param dwOperationCount [in]

The number of elements in the array in <i>pOperations</i>.

### -param pAny [in]

Pointer to extensible data to be added to the body of the request.  This parameter is optional.

### -param ppExpires [out]

Pointer to a pointer to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_eventing_expires">WSD_EVENTING_EXPIRES</a> structure that specfies the duration of the subscription.  Upon completion, call  <a href="/windows/desktop/api/wsdutil/nf-wsdutil-wsdfreelinkedmemory">WSDFreeLinkedMemory</a> to free the memory.   This parameter is optional.

### -param ppAny [out]

Extensible data that the remote device can add to the subscription response. This allows services to provide additional customization of getstatus requests. When done, call  <a href="/windows/desktop/api/wsdutil/nf-wsdutil-wsdfreelinkedmemory">WSDFreeLinkedMemory</a> to free the memory. For details, see <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_element">WSDXML_ELEMENT</a>.  This parameter is optional.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdserviceproxyeventing">IWSDServiceProxyEventing</a>
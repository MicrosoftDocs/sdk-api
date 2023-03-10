---
UID: NF:wsdclient.IWSDEndpointProxy.AbortAsyncOperation
title: IWSDEndpointProxy::AbortAsyncOperation (wsdclient.h)
description: Aborts a pending asynchronous operation.
helpviewer_keywords: ["AbortAsyncOperation","AbortAsyncOperation method","AbortAsyncOperation method","IWSDEndpointProxy interface","IWSDEndpointProxy interface","AbortAsyncOperation method","IWSDEndpointProxy.AbortAsyncOperation","IWSDEndpointProxy::AbortAsyncOperation","ncd.iwsdendpointproxy_abortasyncoperation","wsdclient/IWSDEndpointProxy::AbortAsyncOperation"]
old-location: ncd\iwsdendpointproxy_abortasyncoperation.htm
tech.root: ncd
ms.assetid: 559c7fcd-9652-4dfa-b22a-45929b6aee14
ms.date: 12/05/2018
ms.keywords: AbortAsyncOperation, AbortAsyncOperation method, AbortAsyncOperation method,IWSDEndpointProxy interface, IWSDEndpointProxy interface,AbortAsyncOperation method, IWSDEndpointProxy.AbortAsyncOperation, IWSDEndpointProxy::AbortAsyncOperation, ncd.iwsdendpointproxy_abortasyncoperation, wsdclient/IWSDEndpointProxy::AbortAsyncOperation
req.header: wsdclient.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WsdClient.idl
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
 - IWSDEndpointProxy::AbortAsyncOperation
 - wsdclient/IWSDEndpointProxy::AbortAsyncOperation
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
 - IWSDEndpointProxy.AbortAsyncOperation
---

# IWSDEndpointProxy::AbortAsyncOperation


## -description

Aborts a pending asynchronous operation.

## -parameters

### -param pAsyncResult [in]

Calls the <a href="/windows/desktop/api/wsdclient/nf-wsdclient-iwsdasyncresult-abort">Abort</a> method to end the asynchronous operation.

## -returns

This method can return one of these values.


Possible return values include, but are not limited to, the following.



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
<i>pAsyncResult</i> is <b>NULL</b> or <i>pAsyncResult</i> does not support the <a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdasynccallback">IWSDAsyncCallback</a> interface.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdendpointproxy">IWSDEndpointProxy</a>
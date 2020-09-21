---
UID: NF:wsdclient.IWSDServiceProxy.UnsubscribeToOperation
title: IWSDServiceProxy::UnsubscribeToOperation (wsdclient.h)
description: Cancels a subscription to a notification or solicit/response event.
helpviewer_keywords: ["IWSDServiceProxy interface","UnsubscribeToOperation method","IWSDServiceProxy.UnsubscribeToOperation","IWSDServiceProxy::UnsubscribeToOperation","UnsubscribeToOperation","UnsubscribeToOperation method","UnsubscribeToOperation method","IWSDServiceProxy interface","ncd.iwsdserviceproxy_unsubscribetooperation_method","wsdclient/IWSDServiceProxy::UnsubscribeToOperation"]
old-location: ncd\iwsdserviceproxy_unsubscribetooperation_method.htm
tech.root: ncd
ms.assetid: b306239c-95a4-4a1d-990c-193237bad275
ms.date: 12/05/2018
ms.keywords: IWSDServiceProxy interface,UnsubscribeToOperation method, IWSDServiceProxy.UnsubscribeToOperation, IWSDServiceProxy::UnsubscribeToOperation, UnsubscribeToOperation, UnsubscribeToOperation method, UnsubscribeToOperation method,IWSDServiceProxy interface, ncd.iwsdserviceproxy_unsubscribetooperation_method, wsdclient/IWSDServiceProxy::UnsubscribeToOperation
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
 - IWSDServiceProxy::UnsubscribeToOperation
 - wsdclient/IWSDServiceProxy::UnsubscribeToOperation
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
 - IWSDServiceProxy.UnsubscribeToOperation
---

# IWSDServiceProxy::UnsubscribeToOperation


## -description

Cancels a subscription to a notification or solicit/response event.

## -parameters

### -param pOperation [in]

Reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_operation">WSD_OPERATION</a> structure that specifies the operation subscribed to.

## -returns

Possible return values include, but are not limited to, the following:

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
The proxy is not subscribed to the notification specified by <i>pOperation</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pOperation</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdserviceproxy">IWSDServiceProxy</a>
---
UID: NF:wsdclient.IWSDServiceProxy.SetEventingStatusCallback
title: IWSDServiceProxy::SetEventingStatusCallback (wsdclient.h)
description: Sets or clears the eventing status callback.
helpviewer_keywords: ["IWSDServiceProxy interface","SetEventingStatusCallback method","IWSDServiceProxy.SetEventingStatusCallback","IWSDServiceProxy::SetEventingStatusCallback","SetEventingStatusCallback","SetEventingStatusCallback method","SetEventingStatusCallback method","IWSDServiceProxy interface","ncd.iwsdserviceproxy_seteventingstatuscallback","wsdclient/IWSDServiceProxy::SetEventingStatusCallback"]
old-location: ncd\iwsdserviceproxy_seteventingstatuscallback.htm
tech.root: ncd
ms.assetid: 0a924df4-93a7-4443-a384-0a89d5d90509
ms.date: 12/05/2018
ms.keywords: IWSDServiceProxy interface,SetEventingStatusCallback method, IWSDServiceProxy.SetEventingStatusCallback, IWSDServiceProxy::SetEventingStatusCallback, SetEventingStatusCallback, SetEventingStatusCallback method, SetEventingStatusCallback method,IWSDServiceProxy interface, ncd.iwsdserviceproxy_seteventingstatuscallback, wsdclient/IWSDServiceProxy::SetEventingStatusCallback
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
 - IWSDServiceProxy::SetEventingStatusCallback
 - wsdclient/IWSDServiceProxy::SetEventingStatusCallback
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
 - IWSDServiceProxy.SetEventingStatusCallback
---

# IWSDServiceProxy::SetEventingStatusCallback


## -description

Sets or clears the eventing status callback.

## -parameters

### -param pStatus [in, optional]

An <a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdeventingstatus">IWSDEventingStatus</a> interface that lets the client know of status changes in event subscriptions. If <b>NULL</b>, existing eventing status callbacks are cleared.

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
</table>

## -see-also

<a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdserviceproxy">IWSDServiceProxy</a>
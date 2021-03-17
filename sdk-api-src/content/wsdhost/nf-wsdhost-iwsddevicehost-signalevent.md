---
UID: NF:wsdhost.IWSDDeviceHost.SignalEvent
title: IWSDDeviceHost::SignalEvent (wsdhost.h)
description: Notifies all subscribed clients that an event has occurred.
helpviewer_keywords: ["IWSDDeviceHost interface","SignalEvent method","IWSDDeviceHost.SignalEvent","IWSDDeviceHost::SignalEvent","SignalEvent","SignalEvent method","SignalEvent method","IWSDDeviceHost interface","ncd.iwsddevicehost_signalevent_method","wsdhost/IWSDDeviceHost::SignalEvent"]
old-location: ncd\iwsddevicehost_signalevent_method.htm
tech.root: ncd
ms.assetid: c4cba7f0-6f08-43d7-b255-d3dfb1b5287d
ms.date: 12/05/2018
ms.keywords: IWSDDeviceHost interface,SignalEvent method, IWSDDeviceHost.SignalEvent, IWSDDeviceHost::SignalEvent, SignalEvent, SignalEvent method, SignalEvent method,IWSDDeviceHost interface, ncd.iwsddevicehost_signalevent_method, wsdhost/IWSDDeviceHost::SignalEvent
req.header: wsdhost.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WsdHost.idl
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
 - IWSDDeviceHost::SignalEvent
 - wsdhost/IWSDDeviceHost::SignalEvent
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
 - IWSDDeviceHost.SignalEvent
---

# IWSDDeviceHost::SignalEvent


## -description

Notifies all subscribed clients that an event has occurred.

## -parameters

### -param pszServiceId [in]

The ID of the service that generates the event.

### -param pBody [in]

The body of the event.

### -param pOperation [in]

Reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_operation">WSD_OPERATION</a> structure that specifies the operation.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The host is not started. Call <a href="/windows/desktop/api/wsdhost/nf-wsdhost-iwsddevicehost-start">Start</a> to start the device host.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pszServiceId</i> is <b>NULL</b>, <i>pOperation</i> is <b>NULL</b>, the length in characters of <i>pszServiceId</i> exceeds WSD_MAX_TEXT_LENGTH (8192),  there is no <i>ResponseType</i> structure associated with <i>pOperation</i>, or the service specified by <i>pszServiceId</i> is not subscribed to the event specified by the <i>ResponseType</i> member of <i>pOperation</i>.

</td>
</tr>
</table>

## -remarks

<b>SignalEvent</b> blocks until the event is sent to all clients. Since clients are contacted sequentially, it is possible that <b>SignalEvent</b> will block for a long time if any client responds slowly or is unreachable.

## -see-also

<a href="/windows/desktop/api/wsdhost/nn-wsdhost-iwsddevicehost">IWSDDeviceHost</a>
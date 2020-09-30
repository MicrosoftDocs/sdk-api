---
UID: NF:wsdhost.IWSDDeviceHost.Start
title: IWSDDeviceHost::Start (wsdhost.h)
description: Starts the device host and publishes the device host using a WS-Discovery Hello message.
helpviewer_keywords: ["IWSDDeviceHost interface","Start method","IWSDDeviceHost.Start","IWSDDeviceHost::Start","Start","Start method","Start method","IWSDDeviceHost interface","ncd.iwsddevicehost_start_method","wsdhost/IWSDDeviceHost::Start"]
old-location: ncd\iwsddevicehost_start_method.htm
tech.root: ncd
ms.assetid: 06fea296-2551-46b1-9cd7-54187bca5fe8
ms.date: 12/05/2018
ms.keywords: IWSDDeviceHost interface,Start method, IWSDDeviceHost.Start, IWSDDeviceHost::Start, Start, Start method, Start method,IWSDDeviceHost interface, ncd.iwsddevicehost_start_method, wsdhost/IWSDDeviceHost::Start
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
 - IWSDDeviceHost::Start
 - wsdhost/IWSDDeviceHost::Start
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
 - IWSDDeviceHost.Start
---

# IWSDDeviceHost::Start


## -description

Starts the device host and publishes the device host using a WS-Discovery Hello message. If a notification sink is passed to this method, then the notification sink is also registered. After <b>Start</b> has been called successfully, the device host will automatically respond to Probe and Resolve messages.

## -parameters

### -param ullInstanceId [in]

The instance identifier. If no identifier is provided, the current instance value + 1 is used as the default.

<div class="alert"><b>Note</b>  For compatibility with the WS-Discovery specification, this value must be less than or equal to UINT_MAX (4294967295).</div>
<div> </div>

### -param pScopeList [in]

Scope of the device host. If <b>NULL</b>, no scopes are associated with the host.

### -param pNotificationSink [in, optional]

Reference to an <a href="/windows/desktop/api/wsdhost/nn-wsdhost-iwsddevicehostnotify">IWSDDeviceHostNotify</a> object that specifies the notification sink.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The device host has already been started.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed. It may have failed because the host has not been initialized. Call <a href="/windows/desktop/api/wsdhost/nf-wsdhost-iwsddevicehost-init">Init</a> to initialize a device host.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
There is no metadata associated with the host.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wsdhost/nn-wsdhost-iwsddevicehost">IWSDDeviceHost</a>
---
UID: NF:wsdhost.IWSDDeviceHost.Stop
title: IWSDDeviceHost::Stop (wsdhost.h)
description: Sends a WS-Discovery Bye message and stops the host.
helpviewer_keywords: ["IWSDDeviceHost interface","Stop method","IWSDDeviceHost.Stop","IWSDDeviceHost::Stop","Stop","Stop method","Stop method","IWSDDeviceHost interface","ncd.iwsddevicehost_stop_method","wsdhost/IWSDDeviceHost::Stop"]
old-location: ncd\iwsddevicehost_stop_method.htm
tech.root: ncd
ms.assetid: 7a31e45a-7d38-44b7-84c7-7471bc14cc94
ms.date: 12/05/2018
ms.keywords: IWSDDeviceHost interface,Stop method, IWSDDeviceHost.Stop, IWSDDeviceHost::Stop, Stop, Stop method, Stop method,IWSDDeviceHost interface, ncd.iwsddevicehost_stop_method, wsdhost/IWSDDeviceHost::Stop
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
 - IWSDDeviceHost::Stop
 - wsdhost/IWSDDeviceHost::Stop
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
 - IWSDDeviceHost.Stop
---

# IWSDDeviceHost::Stop


## -description

Sends a WS-Discovery <a href="/windows/desktop/WsdApi/bye-message">Bye</a> message and stops the host. After a host has been successfully stopped, it must be terminated with <a href="/windows/desktop/api/wsdhost/nf-wsdhost-iwsddevicehost-terminate">IWSDDeviceHost::Terminate</a> before being released.



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
The host has already stopped.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The host is not initialized or the host is not started.

</td>
</tr>
</table>

## -remarks

When a device host is stopped using this method, all services remain attached but no inbound messages are processed or otherwise handled. 

Calling <b>Stop</b> is not necessary if the host has not been started.

## -see-also

<a href="/windows/desktop/api/wsdhost/nn-wsdhost-iwsddevicehost">IWSDDeviceHost</a>

---
UID: NF:wsdhost.IWSDDeviceHost.Terminate
title: IWSDDeviceHost::Terminate (wsdhost.h)
description: Terminates the host and releases any attached services.
helpviewer_keywords: ["IWSDDeviceHost interface","Terminate method","IWSDDeviceHost.Terminate","IWSDDeviceHost::Terminate","Terminate","Terminate method","Terminate method","IWSDDeviceHost interface","ncd.iwsddevicehost_terminate","wsdhost/IWSDDeviceHost::Terminate"]
old-location: ncd\iwsddevicehost_terminate.htm
tech.root: ncd
ms.assetid: 2a8df6fb-2834-44f4-9f25-454dcc2ff660
ms.date: 12/05/2018
ms.keywords: IWSDDeviceHost interface,Terminate method, IWSDDeviceHost.Terminate, IWSDDeviceHost::Terminate, Terminate, Terminate method, Terminate method,IWSDDeviceHost interface, ncd.iwsddevicehost_terminate, wsdhost/IWSDDeviceHost::Terminate
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
 - IWSDDeviceHost::Terminate
 - wsdhost/IWSDDeviceHost::Terminate
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
 - IWSDDeviceHost.Terminate
---

# IWSDDeviceHost::Terminate


## -description

Terminates the host and releases any attached services. If a notification sink was passed to the <a href="/windows/desktop/api/wsdhost/nf-wsdhost-iwsddevicehost-start">Start</a> method, then the notification sink is released.



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
The host is uninitialized or the host has already been terminated.

</td>
</tr>
</table>

## -remarks

Services and notification sinks will not receive messages after the <b>Terminate</b> method has completed.

If this device host was started by calling <a href="/windows/desktop/api/wsdhost/nf-wsdhost-iwsddevicehost-start">IWSDDeviceHost::Start</a>, it must first be stopped by calling <a href="/windows/desktop/api/wsdhost/nf-wsdhost-iwsddevicehost-stop">IWSDDeviceHost::Stop</a> before <b>Terminate</b> can be called.

<b>Terminate</b> must be called before releasing the <a href="/windows/desktop/api/wsdhost/nn-wsdhost-iwsddevicehost">IWSDDeviceHost</a>.

## -see-also

<a href="/windows/desktop/api/wsdhost/nn-wsdhost-iwsddevicehost">IWSDDeviceHost</a>

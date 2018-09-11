---
UID: NF:wsdhost.IWSDDeviceHost.Terminate
title: IWSDDeviceHost::Terminate
author: windows-sdk-content
description: Terminates the host and releases any attached services.
old-location: ncd\iwsddevicehost_terminate.htm
tech.root: WsdApi
ms.assetid: 2a8df6fb-2834-44f4-9f25-454dcc2ff660
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IWSDDeviceHost interface,Terminate method, IWSDDeviceHost.Terminate, IWSDDeviceHost::Terminate, Terminate, Terminate method, Terminate method,IWSDDeviceHost interface, ncd.iwsddevicehost_terminate, wsdhost/IWSDDeviceHost::Terminate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDDeviceHost.Terminate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSDDeviceHost::Terminate


## -description


Terminates the host and releases any attached services. If a notification sink was passed to the <a href="https://msdn.microsoft.com/06fea296-2551-46b1-9cd7-54187bca5fe8">Start</a> method, then the notification sink is released.


## -parameters






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

If this device host was started by calling <a href="https://msdn.microsoft.com/06fea296-2551-46b1-9cd7-54187bca5fe8">IWSDDeviceHost::Start</a>, it must first be stopped by calling <a href="https://msdn.microsoft.com/7a31e45a-7d38-44b7-84c7-7471bc14cc94">IWSDDeviceHost::Stop</a> before <b>Terminate</b> can be called.

	<b>Terminate</b> must be called before releasing the <a href="https://msdn.microsoft.com/497d0331-c88d-4381-8990-94227a9b9659">IWSDDeviceHost</a>.





## -see-also




<a href="https://msdn.microsoft.com/497d0331-c88d-4381-8990-94227a9b9659">IWSDDeviceHost</a>
 

 


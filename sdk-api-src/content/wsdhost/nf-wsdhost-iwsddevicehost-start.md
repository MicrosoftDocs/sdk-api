---
UID: NF:wsdhost.IWSDDeviceHost.Start
title: IWSDDeviceHost::Start
author: windows-sdk-content
description: Starts the device host and publishes the device host using a WS-Discovery Hello message.
old-location: ncd\iwsddevicehost_start_method.htm
tech.root: WsdApi
ms.assetid: 06fea296-2551-46b1-9cd7-54187bca5fe8
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IWSDDeviceHost interface,Start method, IWSDDeviceHost.Start, IWSDDeviceHost::Start, Start, Start method, Start method,IWSDDeviceHost interface, ncd.iwsddevicehost_start_method, wsdhost/IWSDDeviceHost::Start
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
 - IWSDDeviceHost.Start
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

Reference to an <a href="https://msdn.microsoft.com/e68e347d-5251-4931-bbcc-7a92b46bf4bd">IWSDDeviceHostNotify</a> object that specifies the notification sink. 


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
The method failed. It may have failed because the host has not been initialized. Call <a href="https://msdn.microsoft.com/a66f0600-0bac-4bef-af43-6db60b60605e">Init</a> to initialize a device host.

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




<a href="https://msdn.microsoft.com/497d0331-c88d-4381-8990-94227a9b9659">IWSDDeviceHost</a>
 

 


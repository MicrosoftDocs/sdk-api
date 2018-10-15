---
UID: NF:windows.media.streaming.IDeviceController.add_DeviceArrival
title: IDeviceController::streaming
author: windows-sdk-content
description: Registers an event handler for the DeviceArrival event.
old-location: mediastreaming\idevicecontroller_add_devicearrival.htm
tech.root: mediastreaming
ms.assetid: 968A30D5-42ED-472B-9436-EBC77A3F76C9
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: IDeviceController interface [Media Streaming API],add_DeviceArrival method, IDeviceController.add_DeviceArrival, IDeviceController.streaming, IDeviceController::add_DeviceArrival, IDeviceController::streaming, add_DeviceArrival, add_DeviceArrival method [Media Streaming API], add_DeviceArrival method [Media Streaming API],IDeviceController interface, mediastreaming.idevicecontroller_add_devicearrival, windows/IDeviceController::add_DeviceArrival
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: windows.media.streaming.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - windows.media.streaming.h
api_name:
 - IDeviceController.add_DeviceArrival
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDeviceController::streaming


## -description


Registers an event handler for the <a href="https://msdn.microsoft.com/C7CB49AE-C05F-4A2A-8A30-4B4BB7C7D9D2">DeviceArrival</a> event.


## -parameters




### -param handler [in]

A <a href="https://msdn.microsoft.com/1a75f230-658c-4418-8fbd-f723f0312b8e">DeviceControllerFinderHandler</a> event handler function.


### -param token [out, retval]

Reference to a token that can be used to unregister the event handler.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



To unregister the event handler that was registered by this method, pass the <i>token</i> value to the <a href="https://msdn.microsoft.com/D1026B13-627C-4FD4-A402-C05E42CF3DCF">remove_DeviceArrival</a> method.




## -see-also




<a href="https://msdn.microsoft.com/18989598-86C5-4BD7-B8F4-27496897DFBA">IDeviceController</a>
 

 


---
UID: NF:windows.media.streaming.IDeviceController.remove_DeviceArrival
title: IDeviceController::streaming (windows.media.streaming.h)
author: windows-sdk-content
description: Unregisters an event handler for the DeviceArrival event.
old-location: mediastreaming\idevicecontroller_remove_devicearrival.htm
tech.root: mediastreaming
ms.assetid: D1026B13-627C-4FD4-A402-C05E42CF3DCF
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDeviceController interface [Media Streaming API],remove_DeviceArrival method, IDeviceController.remove_DeviceArrival, IDeviceController.streaming, IDeviceController::remove_DeviceArrival, IDeviceController::streaming, mediastreaming.idevicecontroller_remove_devicearrival, remove_DeviceArrival, remove_DeviceArrival method [Media Streaming API], remove_DeviceArrival method [Media Streaming API],IDeviceController interface, windows/IDeviceController::remove_DeviceArrival
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
 - IDeviceController.remove_DeviceArrival
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDeviceController::streaming


## -description


Unregisters an event handler for the <a href="https://msdn.microsoft.com/C7CB49AE-C05F-4A2A-8A30-4B4BB7C7D9D2">DeviceArrival</a> event.


## -parameters




### -param token [in]

A reference to a token obtained from the <a href="https://msdn.microsoft.com/968A30D5-42ED-472B-9436-EBC77A3F76C9">add_DeviceArrival</a> method when the event handler was registered.


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
 




## -see-also




<a href="https://msdn.microsoft.com/18989598-86C5-4BD7-B8F4-27496897DFBA">IDeviceController</a>
 

 


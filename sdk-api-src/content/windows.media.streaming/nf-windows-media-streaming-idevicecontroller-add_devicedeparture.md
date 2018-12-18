---
UID: NF:windows.media.streaming.IDeviceController.add_DeviceDeparture
title: IDeviceController::streaming
author: windows-sdk-content
description: Registers an event handler for the DeviceDeparture event.
old-location: mediastreaming\idevicecontroller_add_devicedeparture.htm
tech.root: mediastreaming
ms.assetid: 3DCE2BA9-1F94-45F2-97B7-64BD62B21578
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDeviceController interface [Media Streaming API],add_DeviceDeparture method, IDeviceController.add_DeviceDeparture, IDeviceController.streaming, IDeviceController::add_DeviceDeparture, IDeviceController::streaming, add_DeviceDeparture, add_DeviceDeparture method [Media Streaming API], add_DeviceDeparture method [Media Streaming API],IDeviceController interface, mediastreaming.idevicecontroller_add_devicedeparture, windows/IDeviceController::add_DeviceDeparture
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
 - IDeviceController.add_DeviceDeparture
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDeviceController::streaming


## -description


Registers an event handler for the <a href="https://msdn.microsoft.com/10451878-E685-4042-9F92-BA3A408C4DA0">DeviceDeparture</a> event.


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



To unregister the event handler that was registered by this method, pass the <i>token</i> value to the <a href="https://msdn.microsoft.com/42C7E011-ABC8-493E-853A-0925D2A94118">remove_DeviceDeparture</a> method.




## -see-also




<a href="https://msdn.microsoft.com/18989598-86C5-4BD7-B8F4-27496897DFBA">IDeviceController</a>
 

 


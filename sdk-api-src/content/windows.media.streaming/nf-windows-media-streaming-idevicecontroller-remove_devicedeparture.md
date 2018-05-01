---
UID: NF:windows.media.streaming.IDeviceController.remove_DeviceDeparture
title: IDeviceController::remove_DeviceDeparture method
author: windows-driver-content
description: Unregisters an event handler for the DeviceDeparture event.
old-location: mediastreaming\idevicecontroller_remove_devicedeparture.htm
old-project: mediastreaming
ms.assetid: 42C7E011-ABC8-493E-853A-0925D2A94118
ms.author: windowsdriverdev
ms.date: 4/10/2018
ms.keywords: IDeviceController, IDeviceController interface [Media Streaming API], remove_DeviceDeparture method, IDeviceController::remove_DeviceDeparture, mediastreaming.idevicecontroller_remove_devicedeparture, remove_DeviceDeparture method [Media Streaming API], remove_DeviceDeparture method [Media Streaming API], IDeviceController interface, remove_DeviceDeparture,IDeviceController.remove_DeviceDeparture, windows/IDeviceController::remove_DeviceDeparture
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
req.typenames: TimeSpan
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	windows.media.streaming.h
api_name:
-	IDeviceController.remove_DeviceDeparture
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IDeviceController::remove_DeviceDeparture method


## -description


Unregisters an event handler for the <a href="https://msdn.microsoft.com/10451878-E685-4042-9F92-BA3A408C4DA0">DeviceDeparture</a> event.


## -parameters




### -param token [in]

A reference to a token obtained from the <a href="https://msdn.microsoft.com/3DCE2BA9-1F94-45F2-97B7-64BD62B21578">add_DeviceDeparture</a> method when the event handler was registered.


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
 

 


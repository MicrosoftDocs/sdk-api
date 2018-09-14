---
UID: NF:windows.media.streaming.IDeviceController.AddDevice
title: IDeviceController::streaming
author: windows-sdk-content
description: Adds a DLNA DMR or DMS Device, identified by its UPnP Unique Device Name (UDN), to the list of devices that is returned by the CachedDevices method.
old-location: mediastreaming\idevicecontroller_adddevice.htm
tech.root: mediastreaming
ms.assetid: 9D7DD7C2-21C0-4DD2-BB71-613203097692
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: AddDevice, AddDevice method [Media Streaming API], AddDevice method [Media Streaming API],IDeviceController interface, IDeviceController interface [Media Streaming API],AddDevice method, IDeviceController.AddDevice, IDeviceController.streaming, IDeviceController::AddDevice, IDeviceController::streaming, mediastreaming.idevicecontroller_adddevice, windows/IDeviceController::AddDevice
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
 - IDeviceController.AddDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDeviceController::streaming


## -description


Adds a DLNA DMR or DMS Device, identified by its UPnP Unique Device Name (UDN), to the list of devices that is returned by the <a href="https://msdn.microsoft.com/94C2A7FF-5AF8-4F13-BBA5-54ED78C3BBF6">CachedDevices</a> method.


## -parameters




### -param uniqueDeviceName [in]

A string representing the device’s UDN.


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
 

 


---
UID: NF:windows.media.streaming.IDeviceController.RemoveDevice
title: IDeviceController::streaming
author: windows-sdk-content
description: Removes the specified device from the list of devices that is returned by the CachedDevices method.
old-location: mediastreaming\idevicecontroller_removedevice.htm
tech.root: mediastreaming
ms.assetid: 07002D00-4E7B-4679-A521-A6F4B3148923
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IDeviceController interface [Media Streaming API],RemoveDevice method, IDeviceController.RemoveDevice, IDeviceController.streaming, IDeviceController::RemoveDevice, IDeviceController::streaming, RemoveDevice, RemoveDevice method [Media Streaming API], RemoveDevice method [Media Streaming API],IDeviceController interface, mediastreaming.idevicecontroller_removedevice, windows/IDeviceController::RemoveDevice
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
 - IDeviceController.RemoveDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- windows.media.streaming.h
: 
- IDeviceController.RemoveDevice
: 
---

# IDeviceController::streaming


## -description


Removes the specified device from the list of devices that is returned by the <a href="https://msdn.microsoft.com/94C2A7FF-5AF8-4F13-BBA5-54ED78C3BBF6">CachedDevices</a> method.


## -parameters




### -param device [in]

A reference to an <a href="https://msdn.microsoft.com/E4F99A11-4ED5-44CB-BE16-CBB558412ED4">IBasicDevice</a> that represents the device to remove from the list.


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
 

 


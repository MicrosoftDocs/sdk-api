---
UID: NF:windows.media.streaming.IDeviceController.remove_DeviceArrival
title: IDeviceController::streaming (windows.media.streaming.h)
description: Unregisters an event handler for the DeviceArrival event.
helpviewer_keywords: ["IDeviceController interface [Media Streaming API]","remove_DeviceArrival method","IDeviceController.remove_DeviceArrival","IDeviceController.streaming","IDeviceController::remove_DeviceArrival","IDeviceController::streaming","mediastreaming.idevicecontroller_remove_devicearrival","remove_DeviceArrival","remove_DeviceArrival method [Media Streaming API]","remove_DeviceArrival method [Media Streaming API]","IDeviceController interface","windows/IDeviceController::remove_DeviceArrival"]
old-location: mediastreaming\idevicecontroller_remove_devicearrival.htm
tech.root: mediastreaming
ms.assetid: D1026B13-627C-4FD4-A402-C05E42CF3DCF
ms.date: 12/05/2018
ms.keywords: IDeviceController interface [Media Streaming API],remove_DeviceArrival method, IDeviceController.remove_DeviceArrival, IDeviceController.streaming, IDeviceController::remove_DeviceArrival, IDeviceController::streaming, mediastreaming.idevicecontroller_remove_devicearrival, remove_DeviceArrival, remove_DeviceArrival method [Media Streaming API], remove_DeviceArrival method [Media Streaming API],IDeviceController interface, windows/IDeviceController::remove_DeviceArrival
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDeviceController::remove_DeviceArrival
 - windows.media.streaming/IDeviceController::remove_DeviceArrival
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - windows.media.streaming.h
api_name:
 - IDeviceController.remove_DeviceArrival
---

# IDeviceController::streaming


## -description

Unregisters an event handler for the <a href="/windows/desktop/mediastreaming/devicearrival">DeviceArrival</a> event.

## -parameters

### -param token [in]

A reference to a token obtained from the <a href="/previous-versions/windows/desktop/legacy/hh828903(v=vs.85)">add_DeviceArrival</a> method when the event handler was registered.

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

<a href="/previous-versions/windows/desktop/legacy/hh828901(v=vs.85)">IDeviceController</a>
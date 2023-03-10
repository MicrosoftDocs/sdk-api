---
UID: NF:windows.media.streaming.IDeviceController.add_DeviceArrival
title: IDeviceController::streaming (windows.media.streaming.h)
description: Registers an event handler for the DeviceArrival event.
helpviewer_keywords: ["IDeviceController interface [Media Streaming API]","add_DeviceArrival method","IDeviceController.add_DeviceArrival","IDeviceController.streaming","IDeviceController::add_DeviceArrival","IDeviceController::streaming","add_DeviceArrival","add_DeviceArrival method [Media Streaming API]","add_DeviceArrival method [Media Streaming API]","IDeviceController interface","mediastreaming.idevicecontroller_add_devicearrival","windows/IDeviceController::add_DeviceArrival"]
old-location: mediastreaming\idevicecontroller_add_devicearrival.htm
tech.root: mediastreaming
ms.assetid: 968A30D5-42ED-472B-9436-EBC77A3F76C9
ms.date: 12/05/2018
ms.keywords: IDeviceController interface [Media Streaming API],add_DeviceArrival method, IDeviceController.add_DeviceArrival, IDeviceController.streaming, IDeviceController::add_DeviceArrival, IDeviceController::streaming, add_DeviceArrival, add_DeviceArrival method [Media Streaming API], add_DeviceArrival method [Media Streaming API],IDeviceController interface, mediastreaming.idevicecontroller_add_devicearrival, windows/IDeviceController::add_DeviceArrival
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
 - IDeviceController::add_DeviceArrival
 - windows.media.streaming/IDeviceController::add_DeviceArrival
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
 - IDeviceController.add_DeviceArrival
---

# IDeviceController::streaming


## -description

Registers an event handler for the <a href="/windows/desktop/mediastreaming/devicearrival">DeviceArrival</a> event.

## -parameters

### -param handler [in]

A <a href="/previous-versions/windows/desktop/legacy/hh828843(v=vs.85)">DeviceControllerFinderHandler</a> event handler function.

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

To unregister the event handler that was registered by this method, pass the <i>token</i> value to the <a href="/previous-versions/windows/desktop/legacy/hh828907(v=vs.85)">remove_DeviceArrival</a> method.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/hh828901(v=vs.85)">IDeviceController</a>
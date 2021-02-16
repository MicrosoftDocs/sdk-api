---
UID: NF:windows.media.streaming.IDeviceController.RemoveDevice
title: IDeviceController::streaming (windows.media.streaming.h)
description: Removes the specified device from the list of devices that is returned by the CachedDevices method.
helpviewer_keywords: ["IDeviceController interface [Media Streaming API]","RemoveDevice method","IDeviceController.RemoveDevice","IDeviceController.streaming","IDeviceController::RemoveDevice","IDeviceController::streaming","RemoveDevice","RemoveDevice method [Media Streaming API]","RemoveDevice method [Media Streaming API]","IDeviceController interface","mediastreaming.idevicecontroller_removedevice","windows/IDeviceController::RemoveDevice"]
old-location: mediastreaming\idevicecontroller_removedevice.htm
tech.root: mediastreaming
ms.assetid: 07002D00-4E7B-4679-A521-A6F4B3148923
ms.date: 12/05/2018
ms.keywords: IDeviceController interface [Media Streaming API],RemoveDevice method, IDeviceController.RemoveDevice, IDeviceController.streaming, IDeviceController::RemoveDevice, IDeviceController::streaming, RemoveDevice, RemoveDevice method [Media Streaming API], RemoveDevice method [Media Streaming API],IDeviceController interface, mediastreaming.idevicecontroller_removedevice, windows/IDeviceController::RemoveDevice
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
 - IDeviceController::RemoveDevice
 - windows.media.streaming/IDeviceController::RemoveDevice
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
 - IDeviceController.RemoveDevice
---

# IDeviceController::streaming


## -description

Removes the specified device from the list of devices that is returned by the <a href="/windows/desktop/mediastreaming/idevicecontroller-cacheddevices">CachedDevices</a> method.

## -parameters

### -param device [in]

A reference to an <a href="/windows/desktop/mediastreaming/ibasicdevice">IBasicDevice</a> that represents the device to remove from the list.

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
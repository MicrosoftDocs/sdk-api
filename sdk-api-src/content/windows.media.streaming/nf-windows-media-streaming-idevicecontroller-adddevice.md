---
UID: NF:windows.media.streaming.IDeviceController.AddDevice
title: IDeviceController::streaming (windows.media.streaming.h)
description: Adds a DLNA DMR or DMS Device, identified by its UPnP Unique Device Name (UDN), to the list of devices that is returned by the CachedDevices method.
helpviewer_keywords: ["AddDevice","AddDevice method [Media Streaming API]","AddDevice method [Media Streaming API]","IDeviceController interface","IDeviceController interface [Media Streaming API]","AddDevice method","IDeviceController.AddDevice","IDeviceController.streaming","IDeviceController::AddDevice","IDeviceController::streaming","mediastreaming.idevicecontroller_adddevice","windows/IDeviceController::AddDevice"]
old-location: mediastreaming\idevicecontroller_adddevice.htm
tech.root: mediastreaming
ms.assetid: 9D7DD7C2-21C0-4DD2-BB71-613203097692
ms.date: 12/05/2018
ms.keywords: AddDevice, AddDevice method [Media Streaming API], AddDevice method [Media Streaming API],IDeviceController interface, IDeviceController interface [Media Streaming API],AddDevice method, IDeviceController.AddDevice, IDeviceController.streaming, IDeviceController::AddDevice, IDeviceController::streaming, mediastreaming.idevicecontroller_adddevice, windows/IDeviceController::AddDevice
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
 - IDeviceController::AddDevice
 - windows.media.streaming/IDeviceController::AddDevice
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
 - IDeviceController.AddDevice
---

# IDeviceController::streaming


## -description

Adds a DLNA DMR or DMS Device, identified by its UPnP Unique Device Name (UDN), to the list of devices that is returned by the <a href="/windows/desktop/mediastreaming/idevicecontroller-cacheddevices">CachedDevices</a> method.

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

<a href="/previous-versions/windows/desktop/legacy/hh828901(v=vs.85)">IDeviceController</a>
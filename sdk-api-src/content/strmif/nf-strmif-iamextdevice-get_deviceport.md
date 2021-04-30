---
UID: NF:strmif.IAMExtDevice.get_DevicePort
title: IAMExtDevice::get_DevicePort (strmif.h)
description: The get_DevicePort method retrieves the communication port to which the external device is connected.
helpviewer_keywords: ["IAMExtDevice interface [DirectShow]","get_DevicePort method","IAMExtDevice.get_DevicePort","IAMExtDevice::get_DevicePort","IAMExtDeviceget_DevicePort","dshow.iamextdevice_get_deviceport","get_DevicePort","get_DevicePort method [DirectShow]","get_DevicePort method [DirectShow]","IAMExtDevice interface","strmif/IAMExtDevice::get_DevicePort"]
old-location: dshow\iamextdevice_get_deviceport.htm
tech.root: dshow
ms.assetid: 307ad6ee-1084-4a83-bb19-f766f2328a0d
ms.date: 12/05/2018
ms.keywords: IAMExtDevice interface [DirectShow],get_DevicePort method, IAMExtDevice.get_DevicePort, IAMExtDevice::get_DevicePort, IAMExtDeviceget_DevicePort, dshow.iamextdevice_get_deviceport, get_DevicePort, get_DevicePort method [DirectShow], get_DevicePort method [DirectShow],IAMExtDevice interface, strmif/IAMExtDevice::get_DevicePort
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMExtDevice::get_DevicePort
 - strmif/IAMExtDevice::get_DevicePort
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMExtDevice.get_DevicePort
---

# IAMExtDevice::get_DevicePort


## -description

The <code>get_DevicePort</code> method retrieves the communication port to which the external device is connected.

## -parameters

### -param pDevicePort [out]

Pointer to a <b>long</b> integer that receives one of the following values, indicating the port to which the device is connected:

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>DEV_PORT_1394</td>
<td>IEEE 1394 Bus</td>
</tr>
<tr>
<td>DEV_PORT_ARTI</td>
<td>ARTI driver</td>
</tr>
<tr>
<td>DEV_PORT_COM1</td>
<td>COM1</td>
</tr>
<tr>
<td>DEV_PORT_COM2</td>
<td>COM2</td>
</tr>
<tr>
<td>DEV_PORT_COM3</td>
<td>COM3</td>
</tr>
<tr>
<td>DEV_PORT_COM4</td>
<td>COM4</td>
</tr>
<tr>
<td>DEV_PORT_DIAQ</td>
<td>Diaquest driver</td>
</tr>
<tr>
<td>DEV_PORT_SIM</td>
<td>Simulation port</td>
</tr>
<tr>
<td>DEV_PORT_USB</td>
<td>Universal Serial Bus</td>
</tr>
</table>

## -returns

When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamextdevice">IAMExtDevice Interface</a>
---
UID: NF:portabledeviceapi.IPortableDeviceManager.GetDeviceFriendlyName
title: IPortableDeviceManager::GetDeviceFriendlyName (portabledeviceapi.h)
description: Retrieves the user-friendly name for the device.
helpviewer_keywords: ["GetDeviceFriendlyName","GetDeviceFriendlyName method [Windows Portable Devices SDK]","GetDeviceFriendlyName method [Windows Portable Devices SDK]","IPortableDeviceManager interface","IPortableDeviceManager interface [Windows Portable Devices SDK]","GetDeviceFriendlyName method","IPortableDeviceManager.GetDeviceFriendlyName","IPortableDeviceManager::GetDeviceFriendlyName","IPortableDeviceManagerGetDeviceFriendlyName","portabledeviceapi/IPortableDeviceManager::GetDeviceFriendlyName","wpdsdk.iportabledevicemanager_getdevicefriendlyname"]
old-location: wpdsdk\iportabledevicemanager_getdevicefriendlyname.htm
tech.root: wpdsdk
ms.assetid: 589995bb-fcce-412e-8828-a84e5809af2b
ms.date: 12/05/2018
ms.keywords: GetDeviceFriendlyName, GetDeviceFriendlyName method [Windows Portable Devices SDK], GetDeviceFriendlyName method [Windows Portable Devices SDK],IPortableDeviceManager interface, IPortableDeviceManager interface [Windows Portable Devices SDK],GetDeviceFriendlyName method, IPortableDeviceManager.GetDeviceFriendlyName, IPortableDeviceManager::GetDeviceFriendlyName, IPortableDeviceManagerGetDeviceFriendlyName, portabledeviceapi/IPortableDeviceManager::GetDeviceFriendlyName, wpdsdk.iportabledevicemanager_getdevicefriendlyname
req.header: portabledeviceapi.h
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
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPortableDeviceManager::GetDeviceFriendlyName
 - portabledeviceapi/IPortableDeviceManager::GetDeviceFriendlyName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceGUIDs.lib
 - PortableDeviceGUIDs.dll
api_name:
 - IPortableDeviceManager.GetDeviceFriendlyName
---

# IPortableDeviceManager::GetDeviceFriendlyName


## -description

Retrieves the user-friendly name for the device.

## -parameters

### -param pszPnPDeviceID [in]

Pointer to a null-terminated string that contains the device's Plug and Play ID. You can retrieve a list of Plug and Play names of all devices that are connected to the computer by calling <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicemanager-getdevices">GetDevices</a>.

### -param pDeviceFriendlyName [in, out]

A caller-allocated buffer that is used to hold the user-friendly name for the device. To learn the required size for this parameter, first call this method with this parameter set to <b>NULL</b> and <i>pcchDeviceFriendlyName</i> set to <b>0</b>; the method will succeed and set <i>pcchDeviceFriendlyName</i> to the required buffer size to hold the device-friendly name, including the termination character.

### -param pcchDeviceFriendlyName [in, out]

On input, the maximum number of characters that <i>pDeviceFriendlyName</i> can hold, including the termination character. On output, the number of characters that is returned by <i>pDeviceFriendlyName</i>, also including the termination character.

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
<dt><b>HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER)</b></dt>
</dl>
</td>
<td width="60%">
The supplied buffer is not large enough to hold the device description. (Refer to the value returned in <i>pcchDeviceDescription</i> for the required size.)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_DATA)</b></dt>
</dl>
</td>
<td width="60%">
The device description could not be found.

</td>
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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
At least one of the required arguments was a <b>NULL</b> pointer.

</td>
</tr>
</table>

## -remarks

A device is not required to support this method. If this method fails to retrieve a name, try requesting the <a href="/windows/desktop/wpd_sdk/object-properties">WPD_OBJECT_NAME</a> property of the device object (the object with the ID WPD_DEVICE_OBJECT_ID).

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicemanager">IPortableDeviceManager Interface</a>



<a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicemanager-getdevices">IPortableDeviceManager::GetDevices</a>

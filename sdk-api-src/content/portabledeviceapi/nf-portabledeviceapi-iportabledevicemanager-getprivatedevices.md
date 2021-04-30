---
UID: NF:portabledeviceapi.IPortableDeviceManager.GetPrivateDevices
title: IPortableDeviceManager::GetPrivateDevices (portabledeviceapi.h)
description: The GetPrivateDevices method retrieves a list of private portable devices connected to the computer. These private devices are only accessible through an application that is designed for these particular devices.
helpviewer_keywords: ["GetPrivateDevices","GetPrivateDevices method [Windows Portable Devices SDK]","GetPrivateDevices method [Windows Portable Devices SDK]","IPortableDeviceManager interface","IPortableDeviceManager interface [Windows Portable Devices SDK]","GetPrivateDevices method","IPortableDeviceManager.GetPrivateDevices","IPortableDeviceManager::GetPrivateDevices","IPortableDeviceManagerGetPrivateDevices","portabledeviceapi/IPortableDeviceManager::GetPrivateDevices","wpdsdk.iportabledevicemanager_getprivatedevices"]
old-location: wpdsdk\iportabledevicemanager_getprivatedevices.htm
tech.root: wpdsdk
ms.assetid: f25a8eb4-be40-43c0-bb3c-00031b7f08db
ms.date: 12/05/2018
ms.keywords: GetPrivateDevices, GetPrivateDevices method [Windows Portable Devices SDK], GetPrivateDevices method [Windows Portable Devices SDK],IPortableDeviceManager interface, IPortableDeviceManager interface [Windows Portable Devices SDK],GetPrivateDevices method, IPortableDeviceManager.GetPrivateDevices, IPortableDeviceManager::GetPrivateDevices, IPortableDeviceManagerGetPrivateDevices, portabledeviceapi/IPortableDeviceManager::GetPrivateDevices, wpdsdk.iportabledevicemanager_getprivatedevices
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
 - IPortableDeviceManager::GetPrivateDevices
 - portabledeviceapi/IPortableDeviceManager::GetPrivateDevices
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
 - IPortableDeviceManager.GetPrivateDevices
---

# IPortableDeviceManager::GetPrivateDevices


## -description

The <b>GetPrivateDevices</b> method retrieves a list of private portable devices connected to the computer. These private devices are only accessible through an application that is designed for these particular devices.

## -parameters

### -param pPnPDeviceIDs [in, out]

A caller-allocated array of string pointers that holds the Plug and Play names of all of the connected devices. To learn the required size for this parameter, first call this method with this parameter set to <b>NULL</b> and <i>pcPnPDeviceIDs</i> set to zero, and then allocate a buffer according to the value retrieved by <i>pcPnPDeviceIDs</i>. These names can be used by <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevice-open">IPortableDevice::Open</a> to create a connection to a device.

### -param pcPnPDeviceIDs [in, out]

On input, the number of values that <i>pPnPDeviceIDs</i> can hold. On output, a pointer to the number of devices actually written to <i>pPnPDeviceIDs</i>.

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
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The <i>pPnPDeviceIDs</i> buffer is too small to hold all the values requested, but <i>pcPnPDeviceIDs</i> values have been written to <i>pPnPDeviceIDs</i>.

</td>
</tr>
</table>

## -remarks

In order to write an application that communicates with a private device, you must have knowledge of the custom functionality exposed by a particular device driver. The description of this functionality must be obtained from the device manufacturer.

The list of devices is generated when the device manager is instantiated; it does not refresh as devices connect and disconnect. To refresh the list of connected devices, call <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicemanager-refreshdevicelist">RefreshDeviceList</a>.

The API allocates the memory for each string pointed to by the <i>pPnPDeviceIDs</i> array. Once your application no longer needs these strings, it must iterate through this array and free the associated memory by calling the <b>CoTaskMemFree</b> function.

A private device may not respond correctly to the standard Windows Portable Devices function calls that perform object enumeration, resource transfer, retrieval of device capabilities, and so on.

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicemanager">IPortableDeviceManager Interface</a>
---
UID: NF:portabledeviceapi.IPortableDeviceManager.GetDeviceDescription
title: IPortableDeviceManager::GetDeviceDescription (portabledeviceapi.h)
description: Retrieves the description of a device.
helpviewer_keywords: ["GetDeviceDescription","GetDeviceDescription method [Windows Portable Devices SDK]","GetDeviceDescription method [Windows Portable Devices SDK]","IPortableDeviceManager interface","IPortableDeviceManager interface [Windows Portable Devices SDK]","GetDeviceDescription method","IPortableDeviceManager.GetDeviceDescription","IPortableDeviceManager::GetDeviceDescription","IPortableDeviceManagerGetDeviceDescription","portabledeviceapi/IPortableDeviceManager::GetDeviceDescription","wpdsdk.iportabledevicemanager_getdevicedescription"]
old-location: wpdsdk\iportabledevicemanager_getdevicedescription.htm
tech.root: wpdsdk
ms.assetid: 16c08c8a-9ce7-455a-9859-6b0be406f642
ms.date: 12/05/2018
ms.keywords: GetDeviceDescription, GetDeviceDescription method [Windows Portable Devices SDK], GetDeviceDescription method [Windows Portable Devices SDK],IPortableDeviceManager interface, IPortableDeviceManager interface [Windows Portable Devices SDK],GetDeviceDescription method, IPortableDeviceManager.GetDeviceDescription, IPortableDeviceManager::GetDeviceDescription, IPortableDeviceManagerGetDeviceDescription, portabledeviceapi/IPortableDeviceManager::GetDeviceDescription, wpdsdk.iportabledevicemanager_getdevicedescription
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
 - IPortableDeviceManager::GetDeviceDescription
 - portabledeviceapi/IPortableDeviceManager::GetDeviceDescription
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
 - IPortableDeviceManager.GetDeviceDescription
---

# IPortableDeviceManager::GetDeviceDescription


## -description

Retrieves the description of a device.

## -parameters

### -param pszPnPDeviceID [in]

Pointer to a null-terminated string that contains the device's Plug and Play ID. You can retrieve a list of Plug and Play names of devices that are currently connected by calling <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicemanager-getdevices">GetDevices</a>.

### -param pDeviceDescription [in, out]

A caller-allocated buffer to hold the user-description name of the device. The caller must allocate the memory for this parameter. To learn the required size for this parameter, first call this method with this parameter set to <b>NULL</b> and <i>pcchDeviceDescription</i> set to <b>0</b>; the method will succeed and set <i>pcchDeviceDescription</i> to the required buffer size to hold the device-friendly name, including the termination character.

### -param pcchDeviceDescription [in, out]

The number of characters (not including the termination character) in <i>pDeviceDescription</i>. On input, the maximum length of <i>pDeviceDescription</i>; on output, the length of the returned string in <i>pDeviceDescription</i>.

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

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicemanager-getdevices">GetDevices</a>



<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicemanager">IPortableDeviceManager Interface</a>
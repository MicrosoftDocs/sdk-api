---
UID: NF:portabledeviceapi.IPortableDeviceManager.GetDeviceProperty
title: IPortableDeviceManager::GetDeviceProperty (portabledeviceapi.h)
description: Retrieves a property value stored by the device on the computer. (These are not standard properties that are defined by Windows Portable Devices.).
helpviewer_keywords: ["GetDeviceProperty","GetDeviceProperty method [Windows Portable Devices SDK]","GetDeviceProperty method [Windows Portable Devices SDK]","IPortableDeviceManager interface","IPortableDeviceManager interface [Windows Portable Devices SDK]","GetDeviceProperty method","IPortableDeviceManager.GetDeviceProperty","IPortableDeviceManager::GetDeviceProperty","IPortableDeviceManagerGetDeviceProperty","portabledeviceapi/IPortableDeviceManager::GetDeviceProperty","wpdsdk.iportabledevicemanager_getdeviceproperty"]
old-location: wpdsdk\iportabledevicemanager_getdeviceproperty.htm
tech.root: wpdsdk
ms.assetid: 805a2407-f476-4223-97d9-6d8753380b17
ms.date: 12/05/2018
ms.keywords: GetDeviceProperty, GetDeviceProperty method [Windows Portable Devices SDK], GetDeviceProperty method [Windows Portable Devices SDK],IPortableDeviceManager interface, IPortableDeviceManager interface [Windows Portable Devices SDK],GetDeviceProperty method, IPortableDeviceManager.GetDeviceProperty, IPortableDeviceManager::GetDeviceProperty, IPortableDeviceManagerGetDeviceProperty, portabledeviceapi/IPortableDeviceManager::GetDeviceProperty, wpdsdk.iportabledevicemanager_getdeviceproperty
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
 - IPortableDeviceManager::GetDeviceProperty
 - portabledeviceapi/IPortableDeviceManager::GetDeviceProperty
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
 - IPortableDeviceManager.GetDeviceProperty
---

# IPortableDeviceManager::GetDeviceProperty


## -description

Retrieves a property value stored by the device on the computer. (These are not standard properties that are defined by Windows Portable Devices.)

## -parameters

### -param pszPnPDeviceID [in]

Pointer to a null-terminated string that contains the device's Plug and Play ID. You can retrieve a list of Plug and Play names of all devices that are connected to the computer by calling <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicemanager-getdevices">GetDevices</a>.

### -param pszDevicePropertyName [in]

Pointer to a null-terminated string that contains the name of the property to request. These are custom property names defined by a device manufacturer.

### -param pData [in, out]

A caller-allocated buffer to hold the retrieved data. To get the size required, call this method with this parameter set to <b>NULL</b> and <i>pcbData</i> set to zero, and the required size will be retrieved in <i>pcbData</i>. This call will also return an error that can be ignored. See Return Values.

### -param pcbData [in, out]

The size of the buffer allocated or returned by <i>pData</i>, in bytes.

### -param pdwType [in, out]

A constant describing the type of data returned in <i>pData</i>. The values for this parameter are the same types used to describe the <i>lpType</i> parameter of the Platform SDK function <b>RegQueryValueEx</b>.

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
<dt><b>HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER)</b></dt>
</dl>
</td>
<td width="60%">
The supplied buffer is not large enough to hold the requested data. (This result is always returned when <i>pData</i> is <b>NULL</b>. You can ignore this result if you are calling the method to retrieve the required buffer size. See the description of the <i>pData</i> parameter.)

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

These property values are stored on device installation, or stored by a device during operation so that they can be persisted across connection sessions. An application must know the exact name of the property, which is specified by the device itself; therefore, this method is intended to be used by device developers who are creating their own applications.

To get Windows Portable Devices properties from the device object, call <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceproperties-getvalues">IPortableDeviceProperties::GetValues</a>, and specify the device object with <b>WPD_DEVICE_OBJECT_ID</b>.

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicemanager">IPortableDeviceManager Interface</a>



<a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicemanager-getdevices">IPortableDeviceManager::GetDevices</a>
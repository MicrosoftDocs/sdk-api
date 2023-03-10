---
UID: NF:portabledeviceapi.IPortableDevice.GetPnPDeviceID
title: IPortableDevice::GetPnPDeviceID (portabledeviceapi.h)
description: The GetPnPDeviceID method retrieves the Plug and Play (PnP) device identifier that the application used to open the device.
helpviewer_keywords: ["GetPnPDeviceID","GetPnPDeviceID method [Windows Portable Devices SDK]","GetPnPDeviceID method [Windows Portable Devices SDK]","IPortableDevice interface","IPortableDevice interface [Windows Portable Devices SDK]","GetPnPDeviceID method","IPortableDevice.GetPnPDeviceID","IPortableDevice::GetPnPDeviceID","IPortableDeviceGetPnPDeviceID","portabledeviceapi/IPortableDevice::GetPnPDeviceID","wpdsdk.iportabledevice_getpnpdeviceid"]
old-location: wpdsdk\iportabledevice_getpnpdeviceid.htm
tech.root: wpdsdk
ms.assetid: e6bde2ac-ceef-47f8-b60b-e61595078e8c
ms.date: 12/05/2018
ms.keywords: GetPnPDeviceID, GetPnPDeviceID method [Windows Portable Devices SDK], GetPnPDeviceID method [Windows Portable Devices SDK],IPortableDevice interface, IPortableDevice interface [Windows Portable Devices SDK],GetPnPDeviceID method, IPortableDevice.GetPnPDeviceID, IPortableDevice::GetPnPDeviceID, IPortableDeviceGetPnPDeviceID, portabledeviceapi/IPortableDevice::GetPnPDeviceID, wpdsdk.iportabledevice_getpnpdeviceid
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
 - IPortableDevice::GetPnPDeviceID
 - portabledeviceapi/IPortableDevice::GetPnPDeviceID
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
 - IPortableDevice.GetPnPDeviceID
---

# IPortableDevice::GetPnPDeviceID


## -description

The <b>GetPnPDeviceID</b> method retrieves the Plug and Play (PnP) device identifier that the application used to open the device.

## -parameters

### -param ppszPnPDeviceID [out]

Pointer to a null-terminated string that contains the Plug and Play ID string for the device.

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
<dt><b>E_WPD_DEVICE_NOT_OPEN</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevice-open">IPortableDevice::Open</a> method has not been called yet for this device.

</td>
</tr>
</table>

## -remarks

After the application is through using the string returned by this method, it must call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function to free the string.
      

The <i>ppszPnPDeviceID</i> argument must not be set to <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevice">IPortableDevice Interface</a>



<a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevice-open">IPortableDevice::Open</a>
---
UID: NF:portabledeviceconnectapi.IPortableDeviceConnector.GetPnPID
title: IPortableDeviceConnector::GetPnPID (portabledeviceconnectapi.h)
description: Retrieves the connector's Plug and Play (PnP) device identifier.
helpviewer_keywords: ["GetPnPID","GetPnPID method [Windows Portable Devices SDK]","GetPnPID method [Windows Portable Devices SDK]","IPortableDeviceConnector interface","IPortableDeviceConnector interface [Windows Portable Devices SDK]","GetPnPID method","IPortableDeviceConnector.GetPnPID","IPortableDeviceConnector::GetPnPID","devpkey/IPortableDeviceConnector::GetPnPID","portabledeviceconnectapi/IPortableDeviceConnector::GetPnPID","wpdsdk.iportabledeviceconnector_getpnpid"]
old-location: wpdsdk\iportabledeviceconnector_getpnpid.htm
tech.root: wpdsdk
ms.assetid: 39e7702a-f23e-4f04-8524-06a0fcc025a1
ms.date: 12/05/2018
ms.keywords: GetPnPID, GetPnPID method [Windows Portable Devices SDK], GetPnPID method [Windows Portable Devices SDK],IPortableDeviceConnector interface, IPortableDeviceConnector interface [Windows Portable Devices SDK],GetPnPID method, IPortableDeviceConnector.GetPnPID, IPortableDeviceConnector::GetPnPID, devpkey/IPortableDeviceConnector::GetPnPID, portabledeviceconnectapi/IPortableDeviceConnector::GetPnPID, wpdsdk.iportabledeviceconnector_getpnpid
req.header: portabledeviceconnectapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Portabledeviceconnectapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: PortableDeviceGuids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPortableDeviceConnector::GetPnPID
 - portabledeviceconnectapi/IPortableDeviceConnector::GetPnPID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceGuids.lib
 - PortableDeviceGuids.dll
api_name:
 - IPortableDeviceConnector.GetPnPID
---

# IPortableDeviceConnector::GetPnPID


## -description

The <b>GetPnPID</b> method retrieves the connector's Plug and Play (PnP) device identifier.

## -parameters

### -param ppwszPnPID [out]

The PnP device identifier.

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

The identifier retrieved by this method corresponds to a handle to the MTP/Bluetooth Bus Enumerator device node that receives connect and disconnect IOCTL requests for a paired MTP/Bluetooth device.  Applications can use this identifier with the SetupAPI functions to access the device node.

Once the application no longer needs the identifier specified by the <i>ppwszPnPID</i> parameter, it must call the <b>CoTaskMemAlloc</b> function to free the identifier.

## -see-also

<a href="/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector">IPortableDeviceConnector</a>
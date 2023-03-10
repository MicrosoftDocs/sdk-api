---
UID: NF:portabledeviceapi.IPortableDevice.Capabilities
title: IPortableDevice::Capabilities (portabledeviceapi.h)
description: The Capabilities method retrieves an interface used to query the capabilities of a portable device.
helpviewer_keywords: ["Capabilities","Capabilities method [Windows Portable Devices SDK]","Capabilities method [Windows Portable Devices SDK]","IPortableDevice interface","IPortableDevice interface [Windows Portable Devices SDK]","Capabilities method","IPortableDevice.Capabilities","IPortableDevice::Capabilities","IPortableDeviceCapabilities","portabledeviceapi/IPortableDevice::Capabilities","wpdsdk.iportabledevice_capabilities"]
old-location: wpdsdk\iportabledevice_capabilities.htm
tech.root: wpdsdk
ms.assetid: 3d44e488-1bef-4cdd-bb0b-2b8154deb19e
ms.date: 12/05/2018
ms.keywords: Capabilities, Capabilities method [Windows Portable Devices SDK], Capabilities method [Windows Portable Devices SDK],IPortableDevice interface, IPortableDevice interface [Windows Portable Devices SDK],Capabilities method, IPortableDevice.Capabilities, IPortableDevice::Capabilities, IPortableDeviceCapabilities, portabledeviceapi/IPortableDevice::Capabilities, wpdsdk.iportabledevice_capabilities
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
 - IPortableDevice::Capabilities
 - portabledeviceapi/IPortableDevice::Capabilities
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
 - IPortableDevice.Capabilities
---

# IPortableDevice::Capabilities


## -description

The <b>Capabilities</b> method retrieves an interface used to query the capabilities of a portable device.

## -parameters

### -param ppCapabilities [out]

Address of a variable that receives a pointer to an <a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities">IPortableDeviceCapabilities</a> interface that can describe the device's capabilities. The caller must release this interface when it is done with it.

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
The <i>ppCapabilities</i> argument was a <b>NULL</b> pointer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevice">IPortableDevice Interface</a>



<a href="/windows/desktop/wpd_sdk/retrieving-the-functional-categories-supported-by-a-device">Retrieving the Functional Categories Supported by a Device</a>



<a href="/windows/desktop/wpd_sdk/retrieving-the-rendering-capabilities-supported-by-a-device">Retrieving the Rendering Capabilities Supported by a Device</a>
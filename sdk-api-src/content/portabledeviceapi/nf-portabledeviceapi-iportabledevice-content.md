---
UID: NF:portabledeviceapi.IPortableDevice.Content
title: IPortableDevice::Content (portabledeviceapi.h)
description: The Content method retrieves an interface that you can use to access objects on a device.
helpviewer_keywords: ["Content","Content method [Windows Portable Devices SDK]","Content method [Windows Portable Devices SDK]","IPortableDevice interface","IPortableDevice interface [Windows Portable Devices SDK]","Content method","IPortableDevice.Content","IPortableDevice::Content","IPortableDeviceContent","portabledeviceapi/IPortableDevice::Content","wpdsdk.iportabledevice_content"]
old-location: wpdsdk\iportabledevice_content.htm
tech.root: wpdsdk
ms.assetid: f65ff0b5-ca3b-498f-9c5e-36a76104d220
ms.date: 12/05/2018
ms.keywords: Content, Content method [Windows Portable Devices SDK], Content method [Windows Portable Devices SDK],IPortableDevice interface, IPortableDevice interface [Windows Portable Devices SDK],Content method, IPortableDevice.Content, IPortableDevice::Content, IPortableDeviceContent, portabledeviceapi/IPortableDevice::Content, wpdsdk.iportabledevice_content
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
 - IPortableDevice::Content
 - portabledeviceapi/IPortableDevice::Content
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
 - IPortableDevice.Content
---

# IPortableDevice::Content


## -description

The <b>Content</b> method retrieves an interface that you can use to access objects on a device.

## -parameters

### -param ppContent [out]

Address of a variable that receives a pointer to an <a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent">IPortableDeviceContent</a> interface that is used to access the content on a device. The caller must release this interface when it is done with it.

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
The <i>ppContent</i> argument was a NULL pointer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/wpd_sdk/adding-a-resource-to-an-object">Adding a Resource to an Object</a>



<a href="/windows/desktop/wpd_sdk/enumerating-content">Enumerating Content</a>



<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevice">IPortableDevice Interface</a>



<a href="/windows/desktop/wpd_sdk/moving-content-on-the-device">Moving Content on the Device</a>



<a href="/windows/desktop/wpd_sdk/retrieving-properties-for-multiple-objects">Retrieving Properties for Multiple Objects</a>



<a href="/windows/desktop/wpd_sdk/retrieving-an-object-identifier-from-a-persistent-unique-identifier">Retrieving an Object Identifier from a Persistent Unique Identifier</a>



<a href="/windows/desktop/wpd_sdk/retrieving-the-rendering-capabilities-supported-by-a-device">Retrieving the Rendering Capabilities Supported by a Device</a>



<a href="/windows/desktop/wpd_sdk/setting-properties-for-multiple-objects">Setting Properties for Multiple Objects</a>



<a href="/windows/desktop/wpd_sdk/setting-properties-for-a-single-object">Setting Properties for a Single Object</a>
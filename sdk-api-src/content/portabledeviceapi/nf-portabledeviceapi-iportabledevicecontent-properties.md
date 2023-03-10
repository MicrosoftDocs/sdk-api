---
UID: NF:portabledeviceapi.IPortableDeviceContent.Properties
title: IPortableDeviceContent::Properties (portabledeviceapi.h)
description: The Properties method retrieves the interface that is required to get or set properties on an object on the device.
helpviewer_keywords: ["IPortableDeviceContent interface [Windows Portable Devices SDK]","Properties method","IPortableDeviceContent.Properties","IPortableDeviceContent::Properties","IPortableDeviceContentProperties","Properties","Properties method [Windows Portable Devices SDK]","Properties method [Windows Portable Devices SDK]","IPortableDeviceContent interface","portabledeviceapi/IPortableDeviceContent::Properties","wpdsdk.iportabledevicecontent_properties"]
old-location: wpdsdk\iportabledevicecontent_properties.htm
tech.root: wpdsdk
ms.assetid: bc3ba717-1be3-4f29-ac27-6bdcbc5ed94f
ms.date: 12/05/2018
ms.keywords: IPortableDeviceContent interface [Windows Portable Devices SDK],Properties method, IPortableDeviceContent.Properties, IPortableDeviceContent::Properties, IPortableDeviceContentProperties, Properties, Properties method [Windows Portable Devices SDK], Properties method [Windows Portable Devices SDK],IPortableDeviceContent interface, portabledeviceapi/IPortableDeviceContent::Properties, wpdsdk.iportabledevicecontent_properties
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
 - IPortableDeviceContent::Properties
 - portabledeviceapi/IPortableDeviceContent::Properties
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
 - IPortableDeviceContent.Properties
---

# IPortableDeviceContent::Properties


## -description

The <b>Properties</b> method retrieves the interface that is required to get or set properties on an object on the device.

## -parameters

### -param ppProperties [out]

Address of a variable that receives a pointer to an <a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties">IPortableDeviceProperties</a> interface that is used to get or set object properties. The caller must release this interface when it is done with it.

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
</table>

## -remarks

The retrieved interface is not specific to a particular object on the device; it is specific only to the device. You must specify the ID of the object you want when requesting or setting properties.
      


#### Examples

For an example of how to use this method, see <a href="/windows/desktop/wpd_sdk/setting-properties-for-a-single-object">Setting Properties for a Single Object</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent">IPortableDeviceContent Interface</a>



<a href="/windows/desktop/wpd_sdk/retrieving-content-object-properties">Retrieving Content-Object Properties</a>



<a href="/windows/desktop/wpd_sdk/retrieving-properties-for-multiple-objects">Retrieving Properties for Multiple Objects</a>



<a href="/windows/desktop/wpd_sdk/retrieving-the-rendering-capabilities-supported-by-a-device">Retrieving the Rendering Capabilities Supported by a Device</a>



<a href="/windows/desktop/wpd_sdk/setting-properties-for-multiple-objects">Setting Properties for Multiple Objects</a>



<a href="/windows/desktop/wpd_sdk/setting-properties-for-a-single-object">Setting Properties for a Single Object</a>



<a href="/windows/desktop/wpd_sdk/transferring-content-from-the-device-to-a-pc">Transferring Content from the Device to a PC</a>



<a href="/windows/desktop/wpd_sdk/writing-content-object-properties">Writing Content-Object Properties</a>
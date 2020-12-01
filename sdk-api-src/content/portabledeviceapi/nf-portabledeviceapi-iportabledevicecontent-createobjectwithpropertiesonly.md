---
UID: NF:portabledeviceapi.IPortableDeviceContent.CreateObjectWithPropertiesOnly
title: IPortableDeviceContent::CreateObjectWithPropertiesOnly (portabledeviceapi.h)
description: The CreateObjectWithPropertiesOnly method creates an object with only properties on the device.
helpviewer_keywords: ["CreateObjectWithPropertiesOnly","CreateObjectWithPropertiesOnly method [Windows Portable Devices SDK]","CreateObjectWithPropertiesOnly method [Windows Portable Devices SDK]","IPortableDeviceContent interface","IPortableDeviceContent interface [Windows Portable Devices SDK]","CreateObjectWithPropertiesOnly method","IPortableDeviceContent.CreateObjectWithPropertiesOnly","IPortableDeviceContent::CreateObjectWithPropertiesOnly","IPortableDeviceContentCreateObjectWithPropertiesOnly","portabledeviceapi/IPortableDeviceContent::CreateObjectWithPropertiesOnly","wpdsdk.iportabledevicecontent_createobjectwithpropertiesonly"]
old-location: wpdsdk\iportabledevicecontent_createobjectwithpropertiesonly.htm
tech.root: wpdsdk
ms.assetid: 0695d3d6-1f0d-45b4-8461-a76d759b6c09
ms.date: 12/05/2018
ms.keywords: CreateObjectWithPropertiesOnly, CreateObjectWithPropertiesOnly method [Windows Portable Devices SDK], CreateObjectWithPropertiesOnly method [Windows Portable Devices SDK],IPortableDeviceContent interface, IPortableDeviceContent interface [Windows Portable Devices SDK],CreateObjectWithPropertiesOnly method, IPortableDeviceContent.CreateObjectWithPropertiesOnly, IPortableDeviceContent::CreateObjectWithPropertiesOnly, IPortableDeviceContentCreateObjectWithPropertiesOnly, portabledeviceapi/IPortableDeviceContent::CreateObjectWithPropertiesOnly, wpdsdk.iportabledevicecontent_createobjectwithpropertiesonly
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
 - IPortableDeviceContent::CreateObjectWithPropertiesOnly
 - portabledeviceapi/IPortableDeviceContent::CreateObjectWithPropertiesOnly
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
 - IPortableDeviceContent.CreateObjectWithPropertiesOnly
---

# IPortableDeviceContent::CreateObjectWithPropertiesOnly


## -description

The <b>CreateObjectWithPropertiesOnly</b> method creates an object with only properties on the device.

## -parameters

### -param pValues

An IPortableDeviceValues collection of properties to assign to the object. For a list of required and optional properties for an object, see <a href="/windows/desktop/wpd_sdk/requirements-for-objects">Requirements for Objects</a>.

### -param ppszObjectID [in, out]

An optional string pointer to receive the name of the new object. Can be <b>NULL</b>, if not needed. Windows Portable Devices defines the constant WPD_DEVICE_OBJECT_ID to represent a device. The SDK allocates this memory; the caller must release it using <b>CoTaskMemFree</b>.

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

Some objects are only a collection of properties—such as a folder, which is only a collection of pointers to other objects—while other objects are both properties and data—such as an audio file, which contains all the properties and the actual music bits. This method is used to create an object that contains only properties. To create an object with both properties and data, use <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata">CreateObjectWithPropertiesAndData</a>.
      

This method is synchronous; when it returns, the new object should be present on the device.
      

The object that the driver actually creates might be a properties-and-data object, depending on what type of object is most convenient for the driver. To check what kind of object the driver has created, request the <a href="/windows/desktop/wpd_sdk/object-properties">WPD_OBJECT_FORMAT</a> property of the new object.
      

The object will be created on the device when this method returns.
      


#### Examples

For an example of how to use this method, see <a href="/windows/desktop/wpd_sdk/transferring-a-properties-only-object-to-the-device">Transferring a Properties-Only Object to the Device</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent">IPortableDeviceContent Interface</a>



<a href="/windows/desktop/wpd_sdk/transferring-a-properties-only-object-to-the-device">Transferring a Properties-Only Object to the Device</a>
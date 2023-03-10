---
UID: NF:portabledeviceapi.IPortableDeviceProperties.Delete
title: IPortableDeviceProperties::Delete (portabledeviceapi.h)
description: The Delete method deletes specified properties from a specified object on a device.
helpviewer_keywords: ["Delete","Delete method [Windows Portable Devices SDK]","Delete method [Windows Portable Devices SDK]","IPortableDeviceProperties interface","IPortableDeviceProperties interface [Windows Portable Devices SDK]","Delete method","IPortableDeviceProperties.Delete","IPortableDeviceProperties::Delete","IPortableDevicePropertiesDelete","portabledeviceapi/IPortableDeviceProperties::Delete","wpdsdk.iportabledeviceproperties_delete"]
old-location: wpdsdk\iportabledeviceproperties_delete.htm
tech.root: wpdsdk
ms.assetid: 2547c9aa-edc7-4331-b5f2-bfb4a96f7175
ms.date: 12/05/2018
ms.keywords: Delete, Delete method [Windows Portable Devices SDK], Delete method [Windows Portable Devices SDK],IPortableDeviceProperties interface, IPortableDeviceProperties interface [Windows Portable Devices SDK],Delete method, IPortableDeviceProperties.Delete, IPortableDeviceProperties::Delete, IPortableDevicePropertiesDelete, portabledeviceapi/IPortableDeviceProperties::Delete, wpdsdk.iportabledeviceproperties_delete
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
 - IPortableDeviceProperties::Delete
 - portabledeviceapi/IPortableDeviceProperties::Delete
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
 - IPortableDeviceProperties.Delete
---

# IPortableDeviceProperties::Delete


## -description

The <b>Delete</b> method deletes specified properties from a specified object on a device.

## -parameters

### -param pszObjectID [in]

Pointer to a null-terminated string that specifies the ID of the object whose properties you will delete. To specify the device, use <b>WPD_DEVICE_OBJECT_ID</b>.

### -param pKeys [in]

Pointer to an <a href="/windows/desktop/wpd_sdk/iportabledevicekeycollection">IPortableDeviceKeyCollection</a> interface that specifies which properties to delete. For a list of properties defined by Windows Portable Devices, see <a href="/windows/desktop/wpd_sdk/properties-and-attributes">Properties and Attributes</a>.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
One or more property values could not be deleted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The required pointer argument was <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

Properties can be deleted only if their WPD_PROPERTY_ATTRIBUTE_CAN_DELETE attribute is True. This attribute can be retrieved by calling <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceproperties-getpropertyattributes">GetPropertyAttributes</a>.

The driver has no way to indicate partial success; that is, if only some properties could be deleted, the driver will return <b>S_FALSE</b>, but this method does not indicate which properties were successfully deleted. The only way to learn which properties were deleted is to request all properties by calling <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceproperties-getvalues">IPortableDeviceProperties::GetValues</a>.

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties">IPortableDeviceProperties Interface</a>
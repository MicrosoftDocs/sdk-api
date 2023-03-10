---
UID: NF:portabledeviceapi.IPortableDeviceProperties.GetPropertyAttributes
title: IPortableDeviceProperties::GetPropertyAttributes (portabledeviceapi.h)
description: The GetPropertyAttributes method retrieves attributes of a specified object property on a device.
helpviewer_keywords: ["GetPropertyAttributes","GetPropertyAttributes method [Windows Portable Devices SDK]","GetPropertyAttributes method [Windows Portable Devices SDK]","IPortableDeviceProperties interface","IPortableDeviceProperties interface [Windows Portable Devices SDK]","GetPropertyAttributes method","IPortableDeviceProperties.GetPropertyAttributes","IPortableDeviceProperties::GetPropertyAttributes","IPortableDevicePropertiesGetPropertyAttributes","portabledeviceapi/IPortableDeviceProperties::GetPropertyAttributes","wpdsdk.iportabledeviceproperties_getpropertyattributes"]
old-location: wpdsdk\iportabledeviceproperties_getpropertyattributes.htm
tech.root: wpdsdk
ms.assetid: bb2206ff-e1d4-4bc5-819b-b008a293c43d
ms.date: 12/05/2018
ms.keywords: GetPropertyAttributes, GetPropertyAttributes method [Windows Portable Devices SDK], GetPropertyAttributes method [Windows Portable Devices SDK],IPortableDeviceProperties interface, IPortableDeviceProperties interface [Windows Portable Devices SDK],GetPropertyAttributes method, IPortableDeviceProperties.GetPropertyAttributes, IPortableDeviceProperties::GetPropertyAttributes, IPortableDevicePropertiesGetPropertyAttributes, portabledeviceapi/IPortableDeviceProperties::GetPropertyAttributes, wpdsdk.iportabledeviceproperties_getpropertyattributes
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
 - IPortableDeviceProperties::GetPropertyAttributes
 - portabledeviceapi/IPortableDeviceProperties::GetPropertyAttributes
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
 - IPortableDeviceProperties.GetPropertyAttributes
---

# IPortableDeviceProperties::GetPropertyAttributes


## -description

The <b>GetPropertyAttributes</b> method retrieves attributes of a specified object property on a device.

## -parameters

### -param pszObjectID [in]

Pointer to a null-terminated string that contains the object ID of the object to query. To specify the device, use <b>WPD_DEVICE_OBJECT_ID</b>.

### -param Key [in]

A <b>REFPROPERTYKEY</b> that specifies the property to query for. You can retrieve a list of supported properties by calling <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceproperties-getsupportedproperties">GetSupportedProperties</a>. For a list of properties that are defined by Windows Portable Devices, see <a href="/windows/desktop/wpd_sdk/properties-and-attributes">Properties and Attributes</a>.

### -param ppAttributes [out]

Address of a variable that receives a pointer to an <a href="/windows/desktop/wpd_sdk/iportabledevicevalues">IPortableDeviceValues</a> interface that holds the retrieved property attributes. These are PROPERTYKEY/value pairs, where the <b>PROPERTYKEY</b> is the property, and the value data type depends on the specific property. The caller must release this interface when it is done with it. Attributes defined by Windows Portable Devices can be found on the <a href="/windows/desktop/wpd_sdk/properties-and-attributes">Properties and Attributes</a> page.

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
The method succeeded, and all attributes were retrieved successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Only some attribute values could be retrieved. Others could not, and will contain an <b>HRESULT</b> value of type VT_ERROR.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A required pointer argument was <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

Property attributes describe a property's access rights, valid values, and other information. For example, a property can have a WPD_PROPERTY_ATTRIBUTE_CAN_DELETE value set to False to prevent deletion, and have a range of valid values stored as individual entries.


#### Examples

For an example of how to use this method, see <a href="/windows/desktop/wpd_sdk/setting-properties-for-a-single-object">Setting Properties for a Single Object</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties">IPortableDeviceProperties Interface</a>



<a href="/windows/desktop/wpd_sdk/setting-properties-for-a-single-object">Setting Properties for a Single Object</a>



<a href="/windows/desktop/wpd_sdk/writing-content-object-properties">Writing Content-Object Properties</a>
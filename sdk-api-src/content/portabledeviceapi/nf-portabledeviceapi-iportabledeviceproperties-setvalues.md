---
UID: NF:portabledeviceapi.IPortableDeviceProperties.SetValues
title: IPortableDeviceProperties::SetValues (portabledeviceapi.h)
description: The SetValues method adds or modifies one or more properties on a specified object on a device.
helpviewer_keywords: ["IPortableDeviceProperties interface [Windows Portable Devices SDK]","SetValues method","IPortableDeviceProperties.SetValues","IPortableDeviceProperties::SetValues","IPortableDevicePropertiesSetValues","SetValues","SetValues method [Windows Portable Devices SDK]","SetValues method [Windows Portable Devices SDK]","IPortableDeviceProperties interface","portabledeviceapi/IPortableDeviceProperties::SetValues","wpdsdk.iportabledeviceproperties_setvalues"]
old-location: wpdsdk\iportabledeviceproperties_setvalues.htm
tech.root: wpdsdk
ms.assetid: 3c631d31-5553-4ad0-8384-821c11c78254
ms.date: 12/05/2018
ms.keywords: IPortableDeviceProperties interface [Windows Portable Devices SDK],SetValues method, IPortableDeviceProperties.SetValues, IPortableDeviceProperties::SetValues, IPortableDevicePropertiesSetValues, SetValues, SetValues method [Windows Portable Devices SDK], SetValues method [Windows Portable Devices SDK],IPortableDeviceProperties interface, portabledeviceapi/IPortableDeviceProperties::SetValues, wpdsdk.iportabledeviceproperties_setvalues
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
 - IPortableDeviceProperties::SetValues
 - portabledeviceapi/IPortableDeviceProperties::SetValues
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
 - IPortableDeviceProperties.SetValues
---

# IPortableDeviceProperties::SetValues


## -description

The <b>SetValues</b> method adds or modifies one or more properties on a specified object on a device.

## -parameters

### -param pszObjectID [in]

Pointer to a null-terminated string that contains the object ID of the object to modify. To specify the device, use WPD_DEVICE_OBJECT_ID.

### -param pValues [in]

Pointer to an <a href="/windows/desktop/wpd_sdk/iportabledevicevalues">IPortableDeviceValues</a> interface that contains one or more property/value pairs to set. Existing values will be overwritten.

### -param ppResults [out]

Address of a variable that receives a pointer to an <b>IPortableDeviceValues</b> interface that contains a collection of property/HRESULT values. Each value (type VT_ERROR) describes the success or failure of the property set attempt. The caller must release this interface when it is done with it.

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
All specified property values were updated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
One or more properties could not be modified. Those that could not will have an <b>HRESULT</b> of type VT_ERROR in the retrieved <i>ppResults</i> parameter.

</td>
</tr>
</table>

## -remarks

To delete a property, call <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceproperties-delete">IPortableDeviceProperties::Delete</a>. A property can be deleted only if its WPD_PROPERTY_ATTRIBUTE_CAN_WRITE attribute is True. This attribute can be retrieved by calling <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceproperties-getpropertyattributes">GetPropertyAttributes</a>.


#### Examples

For an example of how to use this method, see <a href="/windows/desktop/wpd_sdk/setting-properties-for-a-single-object">Setting Properties for a Single Object</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties">IPortableDeviceProperties Interface</a>



<a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceproperties-delete">IPortableDeviceProperties::Delete</a>



<a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceproperties-getvalues">IPortableDeviceProperties::GetValues</a>



<a href="/windows/desktop/wpd_sdk/setting-properties-for-a-single-object">Setting Properties for a Single Object</a>



<a href="/windows/desktop/wpd_sdk/writing-content-object-properties">Writing Content-Object Properties</a>
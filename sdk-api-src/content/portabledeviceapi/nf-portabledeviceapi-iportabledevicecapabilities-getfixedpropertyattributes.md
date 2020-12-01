---
UID: NF:portabledeviceapi.IPortableDeviceCapabilities.GetFixedPropertyAttributes
title: IPortableDeviceCapabilities::GetFixedPropertyAttributes (portabledeviceapi.h)
description: The GetFixedPropertyAttributes method retrieves the standard property attributes for a specified property and format.
helpviewer_keywords: ["GetFixedPropertyAttributes","GetFixedPropertyAttributes method [Windows Portable Devices SDK]","GetFixedPropertyAttributes method [Windows Portable Devices SDK]","IPortableDeviceCapabilities interface","IPortableDeviceCapabilities interface [Windows Portable Devices SDK]","GetFixedPropertyAttributes method","IPortableDeviceCapabilities.GetFixedPropertyAttributes","IPortableDeviceCapabilities::GetFixedPropertyAttributes","IPortableDeviceCapabilitiesGetFixedPropertyAttributes","portabledeviceapi/IPortableDeviceCapabilities::GetFixedPropertyAttributes","wpdsdk.iportabledevicecapabilities_getfixedpropertyattributes"]
old-location: wpdsdk\iportabledevicecapabilities_getfixedpropertyattributes.htm
tech.root: wpdsdk
ms.assetid: 94e4e9f4-5858-4e12-bcd7-561fb3636fc8
ms.date: 12/05/2018
ms.keywords: GetFixedPropertyAttributes, GetFixedPropertyAttributes method [Windows Portable Devices SDK], GetFixedPropertyAttributes method [Windows Portable Devices SDK],IPortableDeviceCapabilities interface, IPortableDeviceCapabilities interface [Windows Portable Devices SDK],GetFixedPropertyAttributes method, IPortableDeviceCapabilities.GetFixedPropertyAttributes, IPortableDeviceCapabilities::GetFixedPropertyAttributes, IPortableDeviceCapabilitiesGetFixedPropertyAttributes, portabledeviceapi/IPortableDeviceCapabilities::GetFixedPropertyAttributes, wpdsdk.iportabledevicecapabilities_getfixedpropertyattributes
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
 - IPortableDeviceCapabilities::GetFixedPropertyAttributes
 - portabledeviceapi/IPortableDeviceCapabilities::GetFixedPropertyAttributes
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
 - IPortableDeviceCapabilities.GetFixedPropertyAttributes
---

# IPortableDeviceCapabilities::GetFixedPropertyAttributes


## -description

The <b>GetFixedPropertyAttributes</b> method retrieves the standard property attributes for a specified property and format. Standard attributes are those that have the same value for all objects of the same format. For example, one device might not allow users to modify video file names; this device would return <b>WPD_PROPERTY_ATTRIBUTE_CAN_WRITE</b> with a value of False for WMV formatted objects. Attributes that can have different values for a format, or optional attributes, are not returned.

## -parameters

### -param Format [in]

A <b>REFGUID</b> that specifies the format of the objects of interest. For format <b>GUID</b> values, see <a href="/windows/desktop/wpd_sdk/object-format-guids">Object Formats</a>.

### -param Key [in]

A <b>REFPROPERTYKEY</b> that specifies the property that you want to know the attributes of. Properties defined by Windows Portable Devices are listed in <a href="/windows/desktop/wpd_sdk/properties-and-attributes">Properties and Attributes</a>.

### -param ppAttributes [out]

Address of a variable that receives a pointer to an <a href="/windows/desktop/wpd_sdk/iportabledevicevalues">IPortableDeviceValues</a> interface that holds the attributes and their values. The caller must release this interface when it is done with it.

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

You can specify <b>WPD_OBJECT_FORMAT_ALL</b> for the <i>Format</i> parameter to retrieve the complete set of property attributes.
      

Attributes describe properties. Example attributes are <b>WPD_PROPERTY_ATTRIBUTE_CAN_READ</b> and <b>WPD_PROPERTY_ATTRIBUTE_CAN_WRITE</b>. This method does not retrieve resource attributes.

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities">IPortableDeviceCapabilities Interface</a>



<a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceproperties-getpropertyattributes">IPortableDeviceProperties::GetPropertyAttributes</a>
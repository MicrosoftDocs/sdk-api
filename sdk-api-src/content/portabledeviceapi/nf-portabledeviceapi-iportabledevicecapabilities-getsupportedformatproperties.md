---
UID: NF:portabledeviceapi.IPortableDeviceCapabilities.GetSupportedFormatProperties
title: IPortableDeviceCapabilities::GetSupportedFormatProperties (portabledeviceapi.h)
description: The GetSupportedFormatProperties method retrieves the properties supported by objects of a specified format on the device.
helpviewer_keywords: ["GetSupportedFormatProperties","GetSupportedFormatProperties method [Windows Portable Devices SDK]","GetSupportedFormatProperties method [Windows Portable Devices SDK]","IPortableDeviceCapabilities interface","IPortableDeviceCapabilities interface [Windows Portable Devices SDK]","GetSupportedFormatProperties method","IPortableDeviceCapabilities.GetSupportedFormatProperties","IPortableDeviceCapabilities::GetSupportedFormatProperties","IPortableDeviceCapabilitiesGetSupportedFormatProperties","portabledeviceapi/IPortableDeviceCapabilities::GetSupportedFormatProperties","wpdsdk.iportabledevicecapabilities_getsupportedformatproperties"]
old-location: wpdsdk\iportabledevicecapabilities_getsupportedformatproperties.htm
tech.root: wpdsdk
ms.assetid: 34ea5f04-9cb8-49a2-8d49-14688383c4a6
ms.date: 12/05/2018
ms.keywords: GetSupportedFormatProperties, GetSupportedFormatProperties method [Windows Portable Devices SDK], GetSupportedFormatProperties method [Windows Portable Devices SDK],IPortableDeviceCapabilities interface, IPortableDeviceCapabilities interface [Windows Portable Devices SDK],GetSupportedFormatProperties method, IPortableDeviceCapabilities.GetSupportedFormatProperties, IPortableDeviceCapabilities::GetSupportedFormatProperties, IPortableDeviceCapabilitiesGetSupportedFormatProperties, portabledeviceapi/IPortableDeviceCapabilities::GetSupportedFormatProperties, wpdsdk.iportabledevicecapabilities_getsupportedformatproperties
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
 - IPortableDeviceCapabilities::GetSupportedFormatProperties
 - portabledeviceapi/IPortableDeviceCapabilities::GetSupportedFormatProperties
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
 - IPortableDeviceCapabilities.GetSupportedFormatProperties
---

# IPortableDeviceCapabilities::GetSupportedFormatProperties


## -description

The <b>GetSupportedFormatProperties</b> method retrieves the properties supported by objects of a specified format on the device.

## -parameters

### -param Format [in]

A <b>REFGUID</b> that specifies the format of the object. For a list of formats that are defined by Windows Portable Devices, see <a href="/windows/desktop/wpd_sdk/object-format-guids">Object Formats</a>.

### -param ppKeys [out]

Address of a variable that receives a pointer to an <a href="/windows/desktop/wpd_sdk/iportabledevicekeycollection">IPortableDeviceKeyCollection</a> interface that contains the supported properties for the specified format. For a list of properties defined by Windows Portable Devices, see <a href="/windows/desktop/wpd_sdk/properties-and-attributes">Properties and Attributes</a>. The caller must release this interface when it is done with it.

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
      

If an object does not have a value assigned to a specific property, or if the property was deleted, a device might not report the property at all when enumerating its properties. Another device might report the property, but with an empty string or a value of zero. In order to avoid this inconsistency, you can call this method to learn all the properties you can set on a specific object.

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities">IPortableDeviceCapabilities Interface</a>



<a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedformats">IPortableDeviceCapabilities::GetSupportedFormats</a>
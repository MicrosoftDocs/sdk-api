---
UID: NF:portabledeviceapi.IPortableDeviceCapabilities.GetSupportedFormats
title: IPortableDeviceCapabilities::GetSupportedFormats (portabledeviceapi.h)
description: The GetSupportedFormats method retrieves the supported formats for a specified object type on the device. For example, specifying audio objects might return WPD_OBJECT_FORMAT_WMA, WPD_OBJECT_FORMAT_WAV, and WPD_OBJECT_FORMAT_MP3.
helpviewer_keywords: ["GetSupportedFormats","GetSupportedFormats method [Windows Portable Devices SDK]","GetSupportedFormats method [Windows Portable Devices SDK]","IPortableDeviceCapabilities interface","IPortableDeviceCapabilities interface [Windows Portable Devices SDK]","GetSupportedFormats method","IPortableDeviceCapabilities.GetSupportedFormats","IPortableDeviceCapabilities::GetSupportedFormats","IPortableDeviceCapabilitiesGetSupportedFormats","portabledeviceapi/IPortableDeviceCapabilities::GetSupportedFormats","wpdsdk.iportabledevicecapabilities_getsupportedformats"]
old-location: wpdsdk\iportabledevicecapabilities_getsupportedformats.htm
tech.root: wpdsdk
ms.assetid: 7568f5cf-2f9e-459c-ae08-d23b9e37ce4e
ms.date: 12/05/2018
ms.keywords: GetSupportedFormats, GetSupportedFormats method [Windows Portable Devices SDK], GetSupportedFormats method [Windows Portable Devices SDK],IPortableDeviceCapabilities interface, IPortableDeviceCapabilities interface [Windows Portable Devices SDK],GetSupportedFormats method, IPortableDeviceCapabilities.GetSupportedFormats, IPortableDeviceCapabilities::GetSupportedFormats, IPortableDeviceCapabilitiesGetSupportedFormats, portabledeviceapi/IPortableDeviceCapabilities::GetSupportedFormats, wpdsdk.iportabledevicecapabilities_getsupportedformats
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
 - IPortableDeviceCapabilities::GetSupportedFormats
 - portabledeviceapi/IPortableDeviceCapabilities::GetSupportedFormats
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
 - IPortableDeviceCapabilities.GetSupportedFormats
---

# IPortableDeviceCapabilities::GetSupportedFormats


## -description

The <b>GetSupportedFormats</b> method retrieves the supported formats for a specified object type on the device. For example, specifying audio objects might return <b>WPD_OBJECT_FORMAT_WMA</b>,<b> WPD_OBJECT_FORMAT_WAV</b>, and <b>WPD_OBJECT_FORMAT_MP3</b>.

## -parameters

### -param ContentType [in]

A <b>REFGUID</b> that specifies a content type, such as image, audio, or video. For a list of content types that are defined by Windows Portable Devices, see <a href="/windows/desktop/wpd_sdk/requirements-for-objects">Requirements for Objects</a>.

### -param ppFormats [out]

Address of a variable that receives a pointer to an <a href="/windows/desktop/wpd_sdk/iportabledevicepropvariantcollection">IPortableDevicePropVariantCollection</a> interface that lists the supported formats for the specified content type. These are GUID values (type VT_CLSID) in the retrieved collection items. For a list of formats that are supported by Windows Portable Devices, see <a href="/windows/desktop/wpd_sdk/object-format-guids">Object Formats</a>. The caller must release this interface when it is done with it.

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
At least one of the arguments was a <b>NULL</b> pointer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities">IPortableDeviceCapabilities Interface</a>



<a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedformatproperties">IPortableDeviceCapabilities::GetSupportedFormatProperties</a>
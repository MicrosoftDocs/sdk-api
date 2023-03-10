---
UID: NF:portabledeviceapi.IPortableDeviceCapabilities.GetSupportedContentTypes
title: IPortableDeviceCapabilities::GetSupportedContentTypes (portabledeviceapi.h)
description: The GetSupportedContentTypes method retrieves all supported content types for a specified functional object type on a device.
helpviewer_keywords: ["GetSupportedContentTypes","GetSupportedContentTypes method [Windows Portable Devices SDK]","GetSupportedContentTypes method [Windows Portable Devices SDK]","IPortableDeviceCapabilities interface","IPortableDeviceCapabilities interface [Windows Portable Devices SDK]","GetSupportedContentTypes method","IPortableDeviceCapabilities.GetSupportedContentTypes","IPortableDeviceCapabilities::GetSupportedContentTypes","IPortableDeviceCapabilitiesGetSupportedContentTypes","portabledeviceapi/IPortableDeviceCapabilities::GetSupportedContentTypes","wpdsdk.iportabledevicecapabilities_getsupportedcontenttypes"]
old-location: wpdsdk\iportabledevicecapabilities_getsupportedcontenttypes.htm
tech.root: wpdsdk
ms.assetid: 5f56ca91-552f-4a52-8a68-225601c5f6f4
ms.date: 12/05/2018
ms.keywords: GetSupportedContentTypes, GetSupportedContentTypes method [Windows Portable Devices SDK], GetSupportedContentTypes method [Windows Portable Devices SDK],IPortableDeviceCapabilities interface, IPortableDeviceCapabilities interface [Windows Portable Devices SDK],GetSupportedContentTypes method, IPortableDeviceCapabilities.GetSupportedContentTypes, IPortableDeviceCapabilities::GetSupportedContentTypes, IPortableDeviceCapabilitiesGetSupportedContentTypes, portabledeviceapi/IPortableDeviceCapabilities::GetSupportedContentTypes, wpdsdk.iportabledevicecapabilities_getsupportedcontenttypes
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
 - IPortableDeviceCapabilities::GetSupportedContentTypes
 - portabledeviceapi/IPortableDeviceCapabilities::GetSupportedContentTypes
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
 - IPortableDeviceCapabilities.GetSupportedContentTypes
---

# IPortableDeviceCapabilities::GetSupportedContentTypes


## -description

The <b>GetSupportedContentTypes</b> method retrieves all supported content types for a specified functional object type on a device.

## -parameters

### -param Category [in]

A <b>REFGUID</b> that specifies a functional object category. To get a list of functional categories on the device, call <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicecapabilities-getfunctionalcategories">IPortableDeviceCapabilities::GetFunctionalCategories</a>.

### -param ppContentTypes [out]

Address of a variable that receives a pointer to an <a href="/windows/desktop/wpd_sdk/iportabledevicepropvariantcollection">IPortableDevicePropVariantCollection</a> interface that lists all the supported object types for the specified functional object category. These object types will be <b>GUID</b> values of type VT_CLSID in the retrieved <b>PROPVARIANT</b> items. See <a href="/windows/desktop/wpd_sdk/requirements-for-objects">Requirements for Objects</a> for a list of object types defined by Windows Portable Devices. The caller must release this interface when it is done with it.

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

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities">IPortableDeviceCapabilities Interface</a>



<a href="/windows/desktop/wpd_sdk/retrieving-the-content-types-supported-by-a-device">Retrieving the Content Types Supported by a Device</a>
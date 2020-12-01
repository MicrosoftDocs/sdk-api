---
UID: NF:portabledeviceapi.IPortableDeviceCapabilities.GetFunctionalCategories
title: IPortableDeviceCapabilities::GetFunctionalCategories (portabledeviceapi.h)
description: The GetFunctionalCategories method retrieves all functional categories supported by the device.
helpviewer_keywords: ["GetFunctionalCategories","GetFunctionalCategories method [Windows Portable Devices SDK]","GetFunctionalCategories method [Windows Portable Devices SDK]","IPortableDeviceCapabilities interface","IPortableDeviceCapabilities interface [Windows Portable Devices SDK]","GetFunctionalCategories method","IPortableDeviceCapabilities.GetFunctionalCategories","IPortableDeviceCapabilities::GetFunctionalCategories","IPortableDeviceCapabilitiesGetFunctionalCategories","portabledeviceapi/IPortableDeviceCapabilities::GetFunctionalCategories","wpdsdk.iportabledevicecapabilities_getfunctionalcategories"]
old-location: wpdsdk\iportabledevicecapabilities_getfunctionalcategories.htm
tech.root: wpdsdk
ms.assetid: c444f9d6-7bef-4e0a-bcd8-6a6110986208
ms.date: 12/05/2018
ms.keywords: GetFunctionalCategories, GetFunctionalCategories method [Windows Portable Devices SDK], GetFunctionalCategories method [Windows Portable Devices SDK],IPortableDeviceCapabilities interface, IPortableDeviceCapabilities interface [Windows Portable Devices SDK],GetFunctionalCategories method, IPortableDeviceCapabilities.GetFunctionalCategories, IPortableDeviceCapabilities::GetFunctionalCategories, IPortableDeviceCapabilitiesGetFunctionalCategories, portabledeviceapi/IPortableDeviceCapabilities::GetFunctionalCategories, wpdsdk.iportabledevicecapabilities_getfunctionalcategories
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
 - IPortableDeviceCapabilities::GetFunctionalCategories
 - portabledeviceapi/IPortableDeviceCapabilities::GetFunctionalCategories
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
 - IPortableDeviceCapabilities.GetFunctionalCategories
---

# IPortableDeviceCapabilities::GetFunctionalCategories


## -description

The <b>GetFunctionalCategories</b> method retrieves all functional categories supported by the device.

## -parameters

### -param ppCategories [out]

Address of a variable that receives a pointer to an <a href="/windows/desktop/wpd_sdk/iportabledevicepropvariantcollection">IPortableDevicePropVariantCollection</a> interface that holds all the functional categories for this device. The values will be <b>GUID</b>s  of type VT_CLSID in the retrieved <b>PROPVARIANT</b> values. The caller must release this interface when it is done with it.

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

Functional categories describe the types of functions that a device can perform, such as image capture, audio capture, and storage. This method is typically very fast, because the driver usually queries the device only on startup and caches the results.
      


#### Examples

For an example of how to use this method see <a href="/windows/desktop/wpd_sdk/retrieving-the-functional-categories-supported-by-a-device">Retrieving the Functional Categories Supported by a Device</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities">IPortableDeviceCapabilities Interface</a>



<a href="/windows/desktop/wpd_sdk/retrieving-the-functional-categories-supported-by-a-device">Retrieving the Functional Categories Supported by a Device</a>
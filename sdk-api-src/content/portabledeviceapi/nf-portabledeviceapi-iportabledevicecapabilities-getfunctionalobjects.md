---
UID: NF:portabledeviceapi.IPortableDeviceCapabilities.GetFunctionalObjects
title: IPortableDeviceCapabilities::GetFunctionalObjects (portabledeviceapi.h)
description: The GetFunctionalObjects method retrieves all functional objects that match a specified category on the device.
helpviewer_keywords: ["GetFunctionalObjects","GetFunctionalObjects method [Windows Portable Devices SDK]","GetFunctionalObjects method [Windows Portable Devices SDK]","IPortableDeviceCapabilities interface","IPortableDeviceCapabilities interface [Windows Portable Devices SDK]","GetFunctionalObjects method","IPortableDeviceCapabilities.GetFunctionalObjects","IPortableDeviceCapabilities::GetFunctionalObjects","IPortableDeviceCapabilitiesGetFunctionalObjects","portabledeviceapi/IPortableDeviceCapabilities::GetFunctionalObjects","wpdsdk.iportabledevicecapabilities_getfunctionalobjects"]
old-location: wpdsdk\iportabledevicecapabilities_getfunctionalobjects.htm
tech.root: wpdsdk
ms.assetid: 46657e4d-c2fe-42bf-9a3d-5075d4f3ee91
ms.date: 12/05/2018
ms.keywords: GetFunctionalObjects, GetFunctionalObjects method [Windows Portable Devices SDK], GetFunctionalObjects method [Windows Portable Devices SDK],IPortableDeviceCapabilities interface, IPortableDeviceCapabilities interface [Windows Portable Devices SDK],GetFunctionalObjects method, IPortableDeviceCapabilities.GetFunctionalObjects, IPortableDeviceCapabilities::GetFunctionalObjects, IPortableDeviceCapabilitiesGetFunctionalObjects, portabledeviceapi/IPortableDeviceCapabilities::GetFunctionalObjects, wpdsdk.iportabledevicecapabilities_getfunctionalobjects
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
 - IPortableDeviceCapabilities::GetFunctionalObjects
 - portabledeviceapi/IPortableDeviceCapabilities::GetFunctionalObjects
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
 - IPortableDeviceCapabilities.GetFunctionalObjects
---

# IPortableDeviceCapabilities::GetFunctionalObjects


## -description

The <a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities">GetFunctionalObjects</a> method retrieves all functional objects that match a specified category on the device.

## -parameters

### -param Category [in]

A <b>REFGUID</b> that specifies the category to search for. This can be WPD_FUNCTIONAL_CATEGORY_ALL to return all functional objects.

### -param ppObjectIDs [out]

Address of a variable that receives a pointer to an <a href="/windows/desktop/wpd_sdk/iportabledevicepropvariantcollection">IPortableDevicePropVariantCollection</a> interface that contains the object IDs of the functional objects as strings (type VT_LPWSTR in the retrieved <b>PROPVARIANT</b> items). If no objects of the requested type are found, this will be an empty collection (not <b>NULL</b>). The caller must release this interface when it is done with it.

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

This operation is usually fast, because the driver does not need to perform a full content enumeration, and the number of retrieved functional objects is typically less than 10. If no objects of the requested type are found, this method will not return an error, but returns an empty collection for <i>ppObjectIDs</i>.
      


#### Examples

For an example of how to use this method, see <a href="/windows/desktop/wpd_sdk/retrieving-the-functional-object-identifiers-for-a-device">Retrieving the Functional Object Identifiers for a Device</a>


<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities">IPortableDeviceCapabilities Interface</a>



<a href="/windows/desktop/wpd_sdk/retrieving-the-functional-object-identifiers-for-a-device">Retrieving the Functional Object Identifiers for a Device</a>



<a href="/windows/desktop/wpd_sdk/retrieving-the-rendering-capabilities-supported-by-a-device">Retrieving the Rendering Capabilities Supported by a Device</a>
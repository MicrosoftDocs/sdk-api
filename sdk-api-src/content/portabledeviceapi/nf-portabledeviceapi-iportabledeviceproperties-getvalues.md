---
UID: NF:portabledeviceapi.IPortableDeviceProperties.GetValues
title: IPortableDeviceProperties::GetValues (portabledeviceapi.h)
description: The GetValues method retrieves a list of specified properties from a specified object on a device.
helpviewer_keywords: ["GetValues","GetValues method [Windows Portable Devices SDK]","GetValues method [Windows Portable Devices SDK]","IPortableDeviceProperties interface","IPortableDeviceProperties interface [Windows Portable Devices SDK]","GetValues method","IPortableDeviceProperties.GetValues","IPortableDeviceProperties::GetValues","IPortableDevicePropertiesGetValues","portabledeviceapi/IPortableDeviceProperties::GetValues","wpdsdk.iportabledeviceproperties_getvalues"]
old-location: wpdsdk\iportabledeviceproperties_getvalues.htm
tech.root: wpdsdk
ms.assetid: 5f4ec65c-dd26-40d5-a9f8-a2175c3aa54c
ms.date: 12/05/2018
ms.keywords: GetValues, GetValues method [Windows Portable Devices SDK], GetValues method [Windows Portable Devices SDK],IPortableDeviceProperties interface, IPortableDeviceProperties interface [Windows Portable Devices SDK],GetValues method, IPortableDeviceProperties.GetValues, IPortableDeviceProperties::GetValues, IPortableDevicePropertiesGetValues, portabledeviceapi/IPortableDeviceProperties::GetValues, wpdsdk.iportabledeviceproperties_getvalues
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
 - IPortableDeviceProperties::GetValues
 - portabledeviceapi/IPortableDeviceProperties::GetValues
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
 - IPortableDeviceProperties.GetValues
---

# IPortableDeviceProperties::GetValues


## -description

The <b>GetValues</b> method retrieves a list of specified properties from a specified object on a device.

## -parameters

### -param pszObjectID [in]

Pointer to a null-terminated string that contains the ID of the object to query. To specify the device, use WPD_DEVICE_OBJECT_ID.

### -param pKeys [in]

Pointer to an <a href="/windows/desktop/wpd_sdk/iportabledevicekeycollection">IPortableDeviceKeyCollection</a> interface that contains one or more properties to query for. If this is <b>NULL</b>, all properties will be retrieved. See <a href="/windows/desktop/wpd_sdk/properties-and-attributes">Properties and Attributes</a> for a list of properties that are defined by Windows Portable Devices.

### -param ppValues [out]

Address of a variable that receives a pointer to an <a href="/windows/desktop/wpd_sdk/iportabledevicevalues">IPortableDeviceValues</a> interface that contains the requested property values. These will be returned as PROPERTYKEY/value pairs, where the data type of the value depends on the property. If a value could not be retrieved for some reason, the returned type will be VT_ERROR, and contain an HRESULT value describing the retrieval error. The caller must release this interface when it is done with it.

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
All requested property values were retrieved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
One or more property values could not be retrieved. The problem properties will have an HRESULT value in the retrieved <i>ppValues</i> parameter.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties">IPortableDeviceProperties Interface</a>



<a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceproperties-setvalues">IPortableDeviceProperties::SetValues</a>



<a href="/windows/desktop/wpd_sdk/retrieving-content-object-properties">Retrieving Content-Object Properties</a>



<a href="/windows/desktop/wpd_sdk/retrieving-properties-for-a-single-object">Retrieving Properties for a Single Object</a>



<a href="/windows/desktop/wpd_sdk/retrieving-the-rendering-capabilities-supported-by-a-device">Retrieving the Rendering Capabilities Supported by a Device</a>
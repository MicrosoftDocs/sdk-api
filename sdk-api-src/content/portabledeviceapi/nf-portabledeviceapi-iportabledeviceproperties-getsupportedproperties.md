---
UID: NF:portabledeviceapi.IPortableDeviceProperties.GetSupportedProperties
title: IPortableDeviceProperties::GetSupportedProperties (portabledeviceapi.h)
author: windows-sdk-content
description: The GetSupportedProperties method retrieves a list of properties that a specified object supports. Note that not all of these properties may actually have values.
old-location: wpdsdk\iportabledeviceproperties_getsupportedproperties.htm
tech.root: wpd_sdk
ms.assetid: 0098bfe9-965b-4c70-b28a-d497ac79f44a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetSupportedProperties, GetSupportedProperties method [Windows Portable Devices SDK], GetSupportedProperties method [Windows Portable Devices SDK],IPortableDeviceProperties interface, IPortableDeviceProperties interface [Windows Portable Devices SDK],GetSupportedProperties method, IPortableDeviceProperties.GetSupportedProperties, IPortableDeviceProperties::GetSupportedProperties, IPortableDevicePropertiesGetSupportedProperties, portabledeviceapi/IPortableDeviceProperties::GetSupportedProperties, wpdsdk.iportabledeviceproperties_getsupportedproperties
ms.topic: method
f1_keywords: ["portabledeviceapi/IPortableDeviceProperties.GetSupportedProperties"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceGUIDs.lib
 - PortableDeviceGUIDs.dll
api_name:
 - IPortableDeviceProperties.GetSupportedProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPortableDeviceProperties::GetSupportedProperties


## -description



The <b>GetSupportedProperties</b> method retrieves a list of properties that a specified object supports. Note that not all of these properties may actually have values.




## -parameters




### -param pszObjectID [in]

Pointer to a null-terminated string that contains the object ID of the object to query. To specify the device, use <b>WPD_DEVICE_OBJECT_ID</b>.


### -param ppKeys [out]

Address of a variable that receives a pointer to an <a href="https://docs.microsoft.com/windows/desktop/wpd_sdk/iportabledevicekeycollection">IPortableDeviceKeyCollection</a> interface that contains the supported properties. For a list of properties defined by Windows Portable Devices, see <a href="https://docs.microsoft.com/windows/desktop/wpd_sdk/properties-and-attributes">Properties and Attributes</a>. The caller must release this interface when it is done with it.


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



To get the values of supported properties, call <b>GetPropertyAttributes</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties">IPortableDeviceProperties Interface</a>
 

 


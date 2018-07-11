---
UID: NF:portabledeviceapi.IPortableDeviceProperties.GetValues
title: IPortableDeviceProperties::GetValues
author: windows-sdk-content
description: The GetValues method retrieves a list of specified properties from a specified object on a device.
old-location: wpdsdk\iportabledeviceproperties_getvalues.htm
old-project: wpd_sdk
ms.assetid: 5f4ec65c-dd26-40d5-a9f8-a2175c3aa54c
ms.author: windowssdkdev
ms.date: 04/12/2018
ms.keywords: GetValues, GetValues method [Windows Portable Devices SDK], GetValues method [Windows Portable Devices SDK],IPortableDeviceProperties interface, IPortableDeviceProperties interface [Windows Portable Devices SDK],GetValues method, IPortableDeviceProperties.GetValues, IPortableDeviceProperties::GetValues, IPortableDevicePropertiesGetValues, portabledeviceapi/IPortableDeviceProperties::GetValues, wpdsdk.iportabledeviceproperties_getvalues
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: PNRPINFO_V2, *PPNRPINFO_V2
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
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: ADAM
---

# IPortableDeviceProperties::GetValues


## -description



The <b>GetValues</b> method retrieves a list of specified properties from a specified object on a device.




## -parameters




### -param pszObjectID [in]

Pointer to a null-terminated string that contains the ID of the object to query. To specify the device, use WPD_DEVICE_OBJECT_ID.


### -param pKeys [in]

Pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff597583">IPortableDeviceKeyCollection</a> interface that contains one or more properties to query for. If this is <b>NULL</b>, all properties will be retrieved. See <a href="https://msdn.microsoft.com/3bfbe8d0-6ad5-42de-afdd-d83328aaaa62">Properties and Attributes</a> for a list of properties that are defined by Windows Portable Devices.


### -param ppValues [out]

Address of a variable that receives a pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff597597">IPortableDeviceValues</a> interface that contains the requested property values. These will be returned as PROPERTYKEY/value pairs, where the data type of the value depends on the property. If a value could not be retrieved for some reason, the returned type will be VT_ERROR, and contain an HRESULT value describing the retrieval error. The caller must release this interface when it is done with it.


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




<a href="https://msdn.microsoft.com/4555e85b-c667-466c-a527-cc29ca7a6aee">IPortableDeviceProperties Interface</a>



<a href="https://msdn.microsoft.com/3c631d31-5553-4ad0-8384-821c11c78254">IPortableDeviceProperties::SetValues</a>



<a href="https://msdn.microsoft.com/7fbd6f65-366a-49ea-a680-be77ca0d64f2">Retrieving Content-Object Properties</a>



<a href="https://msdn.microsoft.com/e4e3b286-6330-4147-a367-57accf5beae6">Retrieving Properties for a Single Object</a>



<a href="https://msdn.microsoft.com/2332e3cc-087c-49cf-bde9-7f86f65158e7">Retrieving the Rendering Capabilities Supported by a Device</a>
 

 


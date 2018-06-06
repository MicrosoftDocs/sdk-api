---
UID: NF:portabledeviceconnectapi.IPortableDeviceConnector.SetProperty
title: IPortableDeviceConnector::SetProperty
author: windows-sdk-content
description: Sets the given property on the MTP/Bluetooth Bus Enumerator device.
old-location: wpdsdk\iportabledeviceconnector_setproperty.htm
old-project: wpd_sdk
ms.assetid: 045268e1-3e91-41a9-a14e-eb20b8a707e4
ms.author: windowssdkdev
ms.date: 04/11/2018
ms.keywords: IPortableDeviceConnector interface [Windows Portable Devices SDK],SetProperty method, IPortableDeviceConnector.SetProperty, IPortableDeviceConnector::SetProperty, SetProperty, SetProperty method [Windows Portable Devices SDK], SetProperty method [Windows Portable Devices SDK],IPortableDeviceConnector interface, devpkey/IPortableDeviceConnector::SetProperty, portabledeviceconnectapi/IPortableDeviceConnector::SetProperty, wpdsdk.iportabledeviceconnector_setproperty
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: portabledeviceconnectapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Portabledeviceconnectapi.idl
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
 - PortableDeviceGuids.lib
 - PortableDeviceGuids.dll
api_name:
 - IPortableDeviceConnector.SetProperty
product: Windows
targetos: Windows
req.lib: PortableDeviceGuids.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IPortableDeviceConnector::SetProperty


## -description


The <b>SetProperty</b> method sets the given property on the MTP/Bluetooth Bus Enumerator device.


## -parameters




### -param pPropertyKey [in]

A pointer to a property key for the given property.


### -param PropertyType [in]

The property type.


### -param pData [in]

A pointer to the property data.


### -param cbData [in]

The size (in bytes) of the property data.


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
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
The specified property key is not supported.

</td>
</tr>
</table>
 




## -remarks



Before calling this method, an application must verify that it has Administrator user rights.




## -see-also




<a href="https://msdn.microsoft.com/c6eb1103-2395-431d-9130-1e1f2cc9ae96">IPortableDeviceConnector</a>
 

 


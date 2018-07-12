---
UID: NF:portabledeviceapi.IPortableDeviceResources.GetSupportedResources
title: IPortableDeviceResources::GetSupportedResources
author: windows-sdk-content
description: The GetSupportedResources method retrieves a list of resources that are supported by a specific object.
old-location: wpdsdk\iportabledeviceresources_getsupportedresources.htm
old-project: wpd_sdk
ms.assetid: 415c3256-1385-48d7-999a-91dc3ad795f8
ms.author: windowssdkdev
ms.date: 04/12/2018
ms.keywords: GetSupportedResources, GetSupportedResources method [Windows Portable Devices SDK], GetSupportedResources method [Windows Portable Devices SDK],IPortableDeviceResources interface, IPortableDeviceResources interface [Windows Portable Devices SDK],GetSupportedResources method, IPortableDeviceResources.GetSupportedResources, IPortableDeviceResources::GetSupportedResources, IPortableDeviceResourcesGetSupportedResources, portabledeviceapi/IPortableDeviceResources::GetSupportedResources, wpdsdk.iportabledeviceresources_getsupportedresources
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
 - IPortableDeviceResources.GetSupportedResources
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: ADAM
---

# IPortableDeviceResources::GetSupportedResources


## -description



The <b>GetSupportedResources</b> method retrieves a list of resources that are supported by a specific object.




## -parameters




### -param pszObjectID [in]

Pointer to a null-terminated string that contains the ID of the object.


### -param ppKeys [out]

Address of a variable that receives a pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff597583">IPortableDeviceKeyCollection</a> interface that holds a collection of <b>PROPERTYKEY</b> values specifying resource types supported by this object type. If the object cannot hold resources, this will be an empty collection. The caller must release this interface when it is done with it.


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
At least one of the required pointer arguments was <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The list of resources returned by this method includes all resources that the object <i>can</i> support. This does not mean that all the listed resources actually have data, but that the object is capable of supporting each listed resource.




## -see-also




<a href="https://msdn.microsoft.com/fce2d6db-13f0-4c1d-ba55-16139c6acbb7">IPortableDeviceResources Interface</a>
 

 


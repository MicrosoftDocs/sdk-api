---
UID: NF:portabledeviceapi.IPortableDeviceResources.Delete
title: IPortableDeviceResources::Delete
author: windows-sdk-content
description: The Delete method deletes one or more resources from the object identified by the pszObjectID parameter.
old-location: wpdsdk\iportabledeviceresources_delete.htm
old-project: wpd_sdk
ms.assetid: 3993ebc4-2a8b-48bd-bc93-2e6ad821f5f6
ms.author: windowssdkdev
ms.date: 04/11/2018
ms.keywords: Delete, Delete method [Windows Portable Devices SDK], Delete method [Windows Portable Devices SDK],IPortableDeviceResources interface, IPortableDeviceResources interface [Windows Portable Devices SDK],Delete method, IPortableDeviceResources.Delete, IPortableDeviceResources::Delete, IPortableDeviceResourcesDelete, portabledeviceapi/IPortableDeviceResources::Delete, wpdsdk.iportabledeviceresources_delete
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
 - IPortableDeviceResources.Delete
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IPortableDeviceResources::Delete


## -description



The <b>Delete</b> method deletes one or more resources from the object identified by the <i>pszObjectID</i> parameter.




## -parameters




### -param pszObjectID [in]

Pointer to a null-terminated string that contains the object ID of the object.


### -param pKeys [in]

Pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff597583">IPortableDeviceKeyCollection</a> interface that lists which resources to delete. You can find out what resources the object has by calling <a href="https://msdn.microsoft.com/415c3256-1385-48d7-999a-91dc3ad795f8">GetSupportedResources</a>.


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
 




## -remarks



An object can have several resources. For instance, an object may contain image data, thumbnail image data, and audio data.

An application can retrieve a list of supported resources by calling the <a href="https://msdn.microsoft.com/415c3256-1385-48d7-999a-91dc3ad795f8">GetSupportedResources</a> method.




## -see-also




<a href="https://msdn.microsoft.com/fce2d6db-13f0-4c1d-ba55-16139c6acbb7">IPortableDeviceResources Interface</a>
 

 


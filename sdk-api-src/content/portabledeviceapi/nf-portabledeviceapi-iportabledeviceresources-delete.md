---
UID: NF:portabledeviceapi.IPortableDeviceResources.Delete
title: IPortableDeviceResources::Delete (portabledeviceapi.h)
author: windows-sdk-content
description: The Delete method deletes one or more resources from the object identified by the pszObjectID parameter.
old-location: wpdsdk\iportabledeviceresources_delete.htm
tech.root: wpd_sdk
ms.assetid: 3993ebc4-2a8b-48bd-bc93-2e6ad821f5f6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Delete, Delete method [Windows Portable Devices SDK], Delete method [Windows Portable Devices SDK],IPortableDeviceResources interface, IPortableDeviceResources interface [Windows Portable Devices SDK],Delete method, IPortableDeviceResources.Delete, IPortableDeviceResources::Delete, IPortableDeviceResourcesDelete, portabledeviceapi/IPortableDeviceResources::Delete, wpdsdk.iportabledeviceresources_delete
ms.topic: method
f1_keywords: 
 - "portabledeviceapi/IPortableDeviceResources.Delete"
dev_langs:
 - c++
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
 - IPortableDeviceResources.Delete
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPortableDeviceResources::Delete


## -description



The <b>Delete</b> method deletes one or more resources from the object identified by the <i>pszObjectID</i> parameter.




## -parameters




### -param pszObjectID [in]

Pointer to a null-terminated string that contains the object ID of the object.


### -param pKeys [in]

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/wpd_sdk/iportabledevicekeycollection">IPortableDeviceKeyCollection</a> interface that lists which resources to delete. You can find out what resources the object has by calling <a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceresources-getsupportedresources">GetSupportedResources</a>.


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

An application can retrieve a list of supported resources by calling the <a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceresources-getsupportedresources">GetSupportedResources</a> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceresources">IPortableDeviceResources Interface</a>
 

 


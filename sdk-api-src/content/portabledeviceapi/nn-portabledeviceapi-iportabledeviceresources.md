---
UID: NN:portabledeviceapi.IPortableDeviceResources
title: IPortableDeviceResources (portabledeviceapi.h)
author: windows-sdk-content
description: The IPortableDeviceResources interface provides access to an object's raw data. Use this interface to read or write resources in an object. To get this interface, call IPortableDeviceContent::Transfer.
old-location: wpdsdk\iportabledeviceresources.htm
tech.root: wpd_sdk
ms.assetid: fce2d6db-13f0-4c1d-ba55-16139c6acbb7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPortableDeviceResources, IPortableDeviceResources interface [Windows Portable Devices SDK], IPortableDeviceResources interface [Windows Portable Devices SDK],described, IPortableDeviceResourcesInterface, portabledeviceapi/IPortableDeviceResources, wpdsdk.iportabledeviceresources
ms.topic: interface
f1_keywords: ["portabledeviceapi/IPortableDeviceResources"]
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
 - IPortableDeviceResources
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPortableDeviceResources interface


## -description



The <b>IPortableDeviceResources</b> interface provides access to an object's raw data. Use this interface to read or write resources in an object. To get this interface, call <a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicecontent-transfer">IPortableDeviceContent::Transfer</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPortableDeviceResources</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPortableDeviceResources</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPortableDeviceResources</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceresources-cancel">Cancel</a>
</td>
<td align="left" width="63%">
Cancels a pending operation on this interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceresources-delete">Delete</a>
</td>
<td align="left" width="63%">
Deletes one or more resources from an object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceresources-getresourceattributes">GetResourceAttributes</a>
</td>
<td align="left" width="63%">
Retrieves all attributes from a specified resource in an object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceresources-getstream">GetStream</a>
</td>
<td align="left" width="63%">
Gets an <b>IStream</b> interface with which to read or write the content data in an object on a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceresources-getsupportedresources">GetSupportedResources</a>
</td>
<td align="left" width="63%">
Retrieves a list of resources supported by a specific object.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wpd_sdk/client-interfaces">Client Interfaces</a>
 

 


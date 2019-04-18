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



The <b>IPortableDeviceResources</b> interface provides access to an object's raw data. Use this interface to read or write resources in an object. To get this interface, call <a href="https://msdn.microsoft.com/52fd2ca7-56ba-4e7a-9dcc-5b28f344c1df">IPortableDeviceContent::Transfer</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPortableDeviceResources</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPortableDeviceResources</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/5b36f5bb-43b3-4f2d-87f4-4df842350586">Cancel</a>
</td>
<td align="left" width="63%">
Cancels a pending operation on this interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3993ebc4-2a8b-48bd-bc93-2e6ad821f5f6">Delete</a>
</td>
<td align="left" width="63%">
Deletes one or more resources from an object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6188d0cc-3161-400e-9abf-ef43a4dee690">GetResourceAttributes</a>
</td>
<td align="left" width="63%">
Retrieves all attributes from a specified resource in an object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d5c9a85a-59fa-4b7b-acc7-d450ecd10593">GetStream</a>
</td>
<td align="left" width="63%">
Gets an <b>IStream</b> interface with which to read or write the content data in an object on a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/415c3256-1385-48d7-999a-91dc3ad795f8">GetSupportedResources</a>
</td>
<td align="left" width="63%">
Retrieves a list of resources supported by a specific object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/fbe53f17-940a-485e-82b2-c11ae39b3300">Client Interfaces</a>
 

 


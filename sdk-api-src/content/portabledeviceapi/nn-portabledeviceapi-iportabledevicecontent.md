---
UID: NN:portabledeviceapi.IPortableDeviceContent
title: IPortableDeviceContent
author: windows-sdk-content
description: The IPortableDeviceContent interface provides methods to create, enumerate, examine, and delete content on a device. To get this interface, call IPortableDevice::Content.
old-location: wpdsdk\iportabledevicecontent.htm
old-project: wpd_sdk
ms.assetid: 7a03c673-8e7f-41a4-81ba-88406af2762d
ms.author: windowssdkdev
ms.date: 04/11/2018
ms.keywords: IPortableDeviceContent, IPortableDeviceContent interface [Windows Portable Devices SDK], IPortableDeviceContent interface [Windows Portable Devices SDK],described, portabledeviceapi/IPortableDeviceContent, wpdsdk.iportabledevicecontent
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: PNRPINFO_V2, *PPNRPINFO_V2
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - portabledeviceapi.h
api_name:
 - IPortableDeviceContent
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: ADAM
---

# IPortableDeviceContent interface


## -description



The <b>IPortableDeviceContent</b> interface provides methods to create, enumerate, examine, and delete content on a device. To get this interface, call <b>IPortableDevice::Content</b>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPortableDeviceContent</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPortableDeviceContent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPortableDeviceContent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406716">Cancel</a>
</td>
<td align="left" width="63%">
Cancels a pending call on this interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff544217">Copy</a>
</td>
<td align="left" width="63%">
Copies objects from one location on a device to another.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ea3445cc-69af-40a6-a5a4-695e0f2e1fb6">CreateObjectWithPropertiesAndData</a>
</td>
<td align="left" width="63%">
Creates an object with both properties and data on the device.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0695d3d6-1f0d-45b4-8461-a76d759b6c09">CreateObjectWithPropertiesOnly</a>
</td>
<td align="left" width="63%">
 Creates an object with only properties on the device.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7315c869-d2b6-4ccf-9315-ec1fc1d827ac">Delete</a>
</td>
<td align="left" width="63%">
Deletes one or more objects from the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72526019-58c9-4a18-a925-e0a900f3e35a">EnumObjects</a>
</td>
<td align="left" width="63%">
Rretrieves an interface that is used to enumerate the immediate child objects of an object. It has an optional filter that can enumerate objects with specific properties.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ee2aa718-0616-44b8-a9c6-cc835636500c">GetObjectIDsFromPersistentUniqueIDs</a>
</td>
<td align="left" width="63%">
Retrieves the current object ID of one or more objects, given their persistent unique IDs (PUIDs).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/938a6a06-31c5-44d1-b87b-a108995ae9a1">Move</a>
</td>
<td align="left" width="63%">
Moves one or more objects from one location on the device to another.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff542598">Properties</a>
</td>
<td align="left" width="63%">
Retrieves the interface that is required to get or set properties on an object on the device.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/52fd2ca7-56ba-4e7a-9dcc-5b28f344c1df">Transfer</a>
</td>
<td align="left" width="63%">
Retrieves an interface that is used to read from or write to the content data of an existing object resource.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/fbe53f17-940a-485e-82b2-c11ae39b3300">Client Interfaces</a>
 

 


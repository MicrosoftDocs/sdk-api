---
UID: NN:portabledeviceapi.IPortableDeviceProperties
title: IPortableDeviceProperties
author: windows-sdk-content
description: The IPortableDeviceProperties interface retrieves, adds, or deletes properties from an object on a device, or the device itself.
old-location: wpdsdk\iportabledeviceproperties.htm
old-project: wpd_sdk
ms.assetid: 4555e85b-c667-466c-a527-cc29ca7a6aee
ms.author: windowssdkdev
ms.date: 04/11/2018
ms.keywords: IPortableDeviceProperties, IPortableDeviceProperties interface [Windows Portable Devices SDK], IPortableDeviceProperties interface [Windows Portable Devices SDK],described, IPortableDevicePropertiesInterface, portabledeviceapi/IPortableDeviceProperties, wpdsdk.iportabledeviceproperties
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
 - IPortableDeviceProperties
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: ADAM
---

# IPortableDeviceProperties interface


## -description



The <b>IPortableDeviceProperties</b> interface retrieves, adds, or deletes properties from an object on a device, or the device itself. To get this interface, call <a href="https://msdn.microsoft.com/bc3ba717-1be3-4f29-ac27-6bdcbc5ed94f">IPortableDeviceContent::Properties</a> on an object. To get this interface for the object, specify <b>WPD_DEVICE_OBJECT_ID</b> in <b>GetValues</b>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPortableDeviceProperties</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPortableDeviceProperties</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPortableDeviceProperties</b> interface has these methods.
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
<a href="https://msdn.microsoft.com/2547c9aa-edc7-4331-b5f2-bfb4a96f7175">Delete</a>
</td>
<td align="left" width="63%">
Deletes specified properties from a specified object on a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bb2206ff-e1d4-4bc5-819b-b008a293c43d">GetPropertyAttributes</a>
</td>
<td align="left" width="63%">
Retrieves attributes of a specified object property on a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0098bfe9-965b-4c70-b28a-d497ac79f44a">GetSupportedProperties</a>
</td>
<td align="left" width="63%">
Retrieves a list of properties that a specified object supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff549480">GetValues</a>
</td>
<td align="left" width="63%">
Retrieves a list of specified properties from a specified object on a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556883">SetValues</a>
</td>
<td align="left" width="63%">
Adds or modifies one or more properties on a specified object on a device.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/fbe53f17-940a-485e-82b2-c11ae39b3300">Client Interfaces</a>
 

 


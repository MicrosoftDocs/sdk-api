---
UID: NN:portabledeviceapi.IPortableDeviceContent
title: IPortableDeviceContent (portabledeviceapi.h)
description: The IPortableDeviceContent interface provides methods to create, enumerate, examine, and delete content on a device. To get this interface, call IPortableDevice::Content.
helpviewer_keywords: ["IPortableDeviceContent","IPortableDeviceContent interface [Windows Portable Devices SDK]","IPortableDeviceContent interface [Windows Portable Devices SDK]","described","portabledeviceapi/IPortableDeviceContent","wpdsdk.iportabledevicecontent"]
old-location: wpdsdk\iportabledevicecontent.htm
tech.root: wpd_sdk
ms.assetid: 7a03c673-8e7f-41a4-81ba-88406af2762d
ms.date: 12/05/2018
ms.keywords: IPortableDeviceContent, IPortableDeviceContent interface [Windows Portable Devices SDK], IPortableDeviceContent interface [Windows Portable Devices SDK],described, portabledeviceapi/IPortableDeviceContent, wpdsdk.iportabledevicecontent
f1_keywords:
- portabledeviceapi/IPortableDeviceContent
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- portabledeviceapi.h
api_name:
- IPortableDeviceContent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPortableDeviceContent interface


## -description



The <b>IPortableDeviceContent</b> interface provides methods to create, enumerate, examine, and delete content on a device. To get this interface, call <b>IPortableDevice::Content</b>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPortableDeviceContent</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPortableDeviceContent</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicecontent-cancel">Cancel</a>
</td>
<td align="left" width="63%">
Cancels a pending call on this interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicecontent-copy">Copy</a>
</td>
<td align="left" width="63%">
Copies objects from one location on a device to another.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata">CreateObjectWithPropertiesAndData</a>
</td>
<td align="left" width="63%">
Creates an object with both properties and data on the device.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesonly">CreateObjectWithPropertiesOnly</a>
</td>
<td align="left" width="63%">
 Creates an object with only properties on the device.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicecontent-delete">Delete</a>
</td>
<td align="left" width="63%">
Deletes one or more objects from the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicecontent-enumobjects">EnumObjects</a>
</td>
<td align="left" width="63%">
Rretrieves an interface that is used to enumerate the immediate child objects of an object. It has an optional filter that can enumerate objects with specific properties.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicecontent-getobjectidsfrompersistentuniqueids">GetObjectIDsFromPersistentUniqueIDs</a>
</td>
<td align="left" width="63%">
Retrieves the current object ID of one or more objects, given their persistent unique IDs (PUIDs).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicecontent-move">Move</a>
</td>
<td align="left" width="63%">
Moves one or more objects from one location on the device to another.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicecontent-properties">Properties</a>
</td>
<td align="left" width="63%">
Retrieves the interface that is required to get or set properties on an object on the device.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicecontent-transfer">Transfer</a>
</td>
<td align="left" width="63%">
Retrieves an interface that is used to read from or write to the content data of an existing object resource.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wpd_sdk/client-interfaces">Client Interfaces</a>
 

 


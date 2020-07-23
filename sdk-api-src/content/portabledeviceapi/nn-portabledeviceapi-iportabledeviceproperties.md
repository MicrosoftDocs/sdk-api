---
UID: NN:portabledeviceapi.IPortableDeviceProperties
title: IPortableDeviceProperties (portabledeviceapi.h)
description: The IPortableDeviceProperties interface retrieves, adds, or deletes properties from an object on a device, or the device itself.
helpviewer_keywords: ["IPortableDeviceProperties","IPortableDeviceProperties interface [Windows Portable Devices SDK]","IPortableDeviceProperties interface [Windows Portable Devices SDK]","described","IPortableDevicePropertiesInterface","portabledeviceapi/IPortableDeviceProperties","wpdsdk.iportabledeviceproperties"]
old-location: wpdsdk\iportabledeviceproperties.htm
tech.root: wpdsdk
ms.assetid: 4555e85b-c667-466c-a527-cc29ca7a6aee
ms.date: 12/05/2018
ms.keywords: IPortableDeviceProperties, IPortableDeviceProperties interface [Windows Portable Devices SDK], IPortableDeviceProperties interface [Windows Portable Devices SDK],described, IPortableDevicePropertiesInterface, portabledeviceapi/IPortableDeviceProperties, wpdsdk.iportabledeviceproperties
f1_keywords:
- portabledeviceapi/IPortableDeviceProperties
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
- IPortableDeviceProperties
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPortableDeviceProperties interface


## -description



The <b>IPortableDeviceProperties</b> interface retrieves, adds, or deletes properties from an object on a device, or the device itself. To get this interface, call <a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicecontent-properties">IPortableDeviceContent::Properties</a> on an object. To get this interface for the object, specify <b>WPD_DEVICE_OBJECT_ID</b> in <b>GetValues</b>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPortableDeviceProperties</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPortableDeviceProperties</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceproperties-cancel">Cancel</a>
</td>
<td align="left" width="63%">
Cancels a pending call on this interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceproperties-delete">Delete</a>
</td>
<td align="left" width="63%">
Deletes specified properties from a specified object on a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceproperties-getpropertyattributes">GetPropertyAttributes</a>
</td>
<td align="left" width="63%">
Retrieves attributes of a specified object property on a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceproperties-getsupportedproperties">GetSupportedProperties</a>
</td>
<td align="left" width="63%">
Retrieves a list of properties that a specified object supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceproperties-getvalues">GetValues</a>
</td>
<td align="left" width="63%">
Retrieves a list of specified properties from a specified object on a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceproperties-setvalues">SetValues</a>
</td>
<td align="left" width="63%">
Adds or modifies one or more properties on a specified object on a device.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wpd_sdk/client-interfaces">Client Interfaces</a>
 

 


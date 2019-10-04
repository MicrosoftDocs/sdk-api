---
UID: NN:portabledeviceapi.IPortableDeviceCapabilities
title: IPortableDeviceCapabilities (portabledeviceapi.h)
author: windows-sdk-content
description: The IPortableDeviceCapabilities interface a variety of device capabilities, including supported formats, commands, and functional objects. You can retrieve this interface from a device by calling IPortableDevice::Capabilities.
old-location: wpdsdk\iportabledevicecapabilities.htm
tech.root: wpd_sdk
ms.assetid: c292a509-f202-4136-bbf7-b4e82ef2b936
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPortableDeviceCapabilities, IPortableDeviceCapabilities interface [Windows Portable Devices SDK], IPortableDeviceCapabilities interface [Windows Portable Devices SDK],described, portabledeviceapi/IPortableDeviceCapabilities, wpdsdk.iportabledevicecapabilities
ms.topic: interface
f1_keywords: 
 - "portabledeviceapi/IPortableDeviceCapabilities"
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
 - IPortableDeviceCapabilities
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPortableDeviceCapabilities interface


## -description



The <b>IPortableDeviceCapabilities</b> interface a variety of device capabilities, including supported formats, commands, and functional objects. You can retrieve this interface from a device by calling <b>IPortableDevice::Capabilities</b>.





## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPortableDeviceCapabilities</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPortableDeviceCapabilities</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPortableDeviceCapabilities</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicecapabilities-cancel">Cancel</a>
</td>
<td align="left" width="63%">
Cancels a pending call on this interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicecapabilities-getcommandoptions">GetCommandOptions</a>
</td>
<td align="left" width="63%">
Retrieves all the supported options for the specified command on the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicecapabilities-geteventoptions">GetEventOptions</a>
</td>
<td align="left" width="63%">
Retrieves all the supported options for the specified event on the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicecapabilities-getfixedpropertyattributes">GetFixedPropertyAttributes</a>
</td>
<td align="left" width="63%">
Retrieves the standard property attributes for a specified property and format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicecapabilities-getfunctionalcategories">GetFunctionalCategories</a>
</td>
<td align="left" width="63%">
Retrieves all functional categories supported by the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicecapabilities-getfunctionalobjects">GetFunctionalObjects</a>
</td>
<td align="left" width="63%">
 Retrieves all functional objects that match a specified category on the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedcommands">GetSupportedCommands</a>
</td>
<td align="left" width="63%">
Retrieves a list of all the supported commands for this device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedcontenttypes">GetSupportedContentTypes</a>
</td>
<td align="left" width="63%">
Retrieves all supported content types for a specified functional object type on a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedevents">GetSupportedEvents</a>
</td>
<td align="left" width="63%">
Retrieves the supported events for this device.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedformatproperties">GetSupportedFormatProperties</a>
</td>
<td align="left" width="63%">
Retrieves the properties supported by objects of a specified format on the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedformats">GetSupportedFormats</a>
</td>
<td align="left" width="63%">
Retrieves the supported formats for a specified object type on the device.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wpd_sdk/client-interfaces">Client Interfaces</a>
 

 


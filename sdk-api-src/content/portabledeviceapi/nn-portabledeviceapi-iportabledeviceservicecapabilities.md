---
UID: NN:portabledeviceapi.IPortableDeviceServiceCapabilities
title: IPortableDeviceServiceCapabilities (portabledeviceapi.h)
author: windows-sdk-content
description: Retrieves information describing the capabilities of a service.
old-location: wpdsdk\iportabledeviceservicecapabilities.htm
tech.root: wpd_sdk
ms.assetid: d472d31c-90da-4ecc-9cf7-4474457a244f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPortableDeviceServiceCapabilities, IPortableDeviceServiceCapabilities interface [Windows Portable Devices SDK], IPortableDeviceServiceCapabilities interface [Windows Portable Devices SDK],described, portabledeviceapi/IPortableDeviceServiceCapabilities, wpdsdk.iportabledeviceservicecapabilities
ms.topic: interface
f1_keywords: 
 - "portabledeviceapi/IPortableDeviceServiceCapabilities"
req.header: portabledeviceapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: PortableDeviceAPI.idl
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
 - PortableDeviceAPI.h
api_name:
 - IPortableDeviceServiceCapabilities
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPortableDeviceServiceCapabilities interface


## -description


The <b>IPortableDeviceServiceCapabilities</b> interface retrieves information describing the capabilities of a  service.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPortableDeviceServiceCapabilities</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPortableDeviceServiceCapabilities</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPortableDeviceServiceCapabilities</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceservicecapabilities-cancel">Cancel</a>
</td>
<td align="left" width="63%">
Cancels a pending operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceservicecapabilities-getcommandoptions">GetCommandOptions</a>
</td>
<td align="left" width="63%">
Retrieves the options of a command.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes">GetEventAttributes</a>
</td>
<td align="left" width="63%">
Retrieves the attributes of an event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventparameterattributes">GetEventParameterAttributes</a>
</td>
<td align="left" width="63%">
Retrieves the attributes of an event parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes">GetFormatAttributes</a>
</td>
<td align="left" width="63%">
Retrieves the attributes of a format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatpropertyattributes">GetFormatPropertyAttributes</a>
</td>
<td align="left" width="63%">
Retrieves the attributes of a format property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatrenderingprofiles">GetFormatRenderingProfiles</a>
</td>
<td align="left" width="63%">
Retrieves the rendering profiles of a format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceservicecapabilities-getinheritedservices">GetInheritedServices</a>
</td>
<td align="left" width="63%">
Retrieves the services having the specified inheritance type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes">GetMethodAttributes</a>
</td>
<td align="left" width="63%">
Retrieves the attributes of a method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodparameterattributes">GetMethodParameterAttributes</a>
</td>
<td align="left" width="63%">
Retrieves the attributes of a method parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedcommands">GetSupportedCommands</a>
</td>
<td align="left" width="63%">
Retrieves the commands supported by the service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedevents">GetSupportedEvents</a>
</td>
<td align="left" width="63%">
Retrieves the events supported by the service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedformatproperties">GetSupportedFormatProperties</a>
</td>
<td align="left" width="63%">
Retrieves the properties supported by the service for the specified format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedformats">GetSupportedFormats</a>
</td>
<td align="left" width="63%">
Retrieves the formats supported by the service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods">GetSupportedMethods</a>
</td>
<td align="left" width="63%">
Retrieves the methods supported by the service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethodsbyformat">GetSupportedMethodsByFormat</a>
</td>
<td align="left" width="63%">
Retrieves the methods supported by the service for the specified format.

</td>
</tr>
</table> 


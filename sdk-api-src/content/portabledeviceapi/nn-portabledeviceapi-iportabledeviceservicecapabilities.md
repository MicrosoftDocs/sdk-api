---
UID: NN:portabledeviceapi.IPortableDeviceServiceCapabilities
title: IPortableDeviceServiceCapabilities
author: windows-sdk-content
description: Retrieves information describing the capabilities of a service.
old-location: wpdsdk\iportabledeviceservicecapabilities.htm
tech.root: wpd_sdk
ms.assetid: d472d31c-90da-4ecc-9cf7-4474457a244f
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IPortableDeviceServiceCapabilities, IPortableDeviceServiceCapabilities interface [Windows Portable Devices SDK], IPortableDeviceServiceCapabilities interface [Windows Portable Devices SDK],described, portabledeviceapi/IPortableDeviceServiceCapabilities, wpdsdk.iportabledeviceservicecapabilities
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
---

# IPortableDeviceServiceCapabilities interface


## -description


The <b>IPortableDeviceServiceCapabilities</b> interface retrieves information describing the capabilities of a  service.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPortableDeviceServiceCapabilities</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPortableDeviceServiceCapabilities</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/f83a23ab-88c4-4486-adad-2bdff6b34df9">Cancel</a>
</td>
<td align="left" width="63%">
Cancels a pending operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5baa4c94-771a-430f-a963-800e4cd3a6b3">GetCommandOptions</a>
</td>
<td align="left" width="63%">
Retrieves the options of a command.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cd3316aa-6d49-4d26-9ded-c9371ebea27b">GetEventAttributes</a>
</td>
<td align="left" width="63%">
Retrieves the attributes of an event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f842dc94-440f-4488-80e3-b10bf72e6269">GetEventParameterAttributes</a>
</td>
<td align="left" width="63%">
Retrieves the attributes of an event parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9fecc9e8-cc5c-4a5f-b5b4-71c63631948d">GetFormatAttributes</a>
</td>
<td align="left" width="63%">
Retrieves the attributes of a format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a4120cfd-500d-47dd-87e9-418a32722332">GetFormatPropertyAttributes</a>
</td>
<td align="left" width="63%">
Retrieves the attributes of a format property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/38c9d357-17aa-4b26-9c01-c13a5cfcf495">GetFormatRenderingProfiles</a>
</td>
<td align="left" width="63%">
Retrieves the rendering profiles of a format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f5640d6a-6c2f-4bd3-adff-628017f5b867">GetInheritedServices</a>
</td>
<td align="left" width="63%">
Retrieves the services having the specified inheritance type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4cd125ea-545f-461b-90e1-88d3e3a6c032">GetMethodAttributes</a>
</td>
<td align="left" width="63%">
Retrieves the attributes of a method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/48c566e1-981f-4173-ad5b-a7b1b7c35d06">GetMethodParameterAttributes</a>
</td>
<td align="left" width="63%">
Retrieves the attributes of a method parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b116ae11-f02f-47aa-8c54-4810e2d50046">GetSupportedCommands</a>
</td>
<td align="left" width="63%">
Retrieves the commands supported by the service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/19621abc-34df-4c16-8cb7-f0d9d7fb7e06">GetSupportedEvents</a>
</td>
<td align="left" width="63%">
Retrieves the events supported by the service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/80ce7975-c567-4c99-9eb5-6d494a0f1883">GetSupportedFormatProperties</a>
</td>
<td align="left" width="63%">
Retrieves the properties supported by the service for the specified format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1df1ed1b-d231-4327-84eb-1bcf74dd881b">GetSupportedFormats</a>
</td>
<td align="left" width="63%">
Retrieves the formats supported by the service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/60201d12-5a49-4d84-9dae-b04cbb144d8f">GetSupportedMethods</a>
</td>
<td align="left" width="63%">
Retrieves the methods supported by the service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f1950aa5-2316-4409-a7bd-1b87c6449187">GetSupportedMethodsByFormat</a>
</td>
<td align="left" width="63%">
Retrieves the methods supported by the service for the specified format.

</td>
</tr>
</table> 


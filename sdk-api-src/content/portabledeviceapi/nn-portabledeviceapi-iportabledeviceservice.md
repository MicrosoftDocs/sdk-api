---
UID: NN:portabledeviceapi.IPortableDeviceService
title: IPortableDeviceService (portabledeviceapi.h)
author: windows-sdk-content
description: Provides access to a service.
old-location: wpdsdk\iportabledeviceservice.htm
tech.root: wpd_sdk
ms.assetid: f57344d5-c978-4c27-b8a9-b42492bd9312
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IPortableDeviceService, IPortableDeviceService interface [Windows Portable Devices SDK], IPortableDeviceService interface [Windows Portable Devices SDK],described, portabledeviceapi/IPortableDeviceService, wpdsdk.iportabledeviceservice
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
 - IPortableDeviceService
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPortableDeviceService interface


## -description


The <b>IPortableDeviceService</b> interface provides access to a service.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPortableDeviceService</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPortableDeviceService</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPortableDeviceService</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/128b1ee9-fd1f-4480-ae9a-b1d0bc86cf1b">Advise</a>
</td>
<td align="left" width="63%">
Registers an application-defined callback object that receives service events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1fb07c56-4e7a-4c20-8e1e-65d8a2c719ab">Cancel</a>
</td>
<td align="left" width="63%">
Cancels a pending service operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/62ef0c63-2908-458f-8e9f-eb6150441380">Capabilities</a>
</td>
<td align="left" width="63%">
Retrieves the service capabilities.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/59cfe8d7-47ce-4d1a-a53a-30f398100aa7">Close</a>
</td>
<td align="left" width="63%">
Releases the connection to the service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/36977b23-b03f-48bc-8313-ddfe2ef208de">Content</a>
</td>
<td align="left" width="63%">
Retrieves access to the service content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c73261a5-1436-4706-8d8b-ff8183429ac4">GetPnPServiceId</a>
</td>
<td align="left" width="63%">
Retrieves a Plug and Play (PnP) identifier for the service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f86907c4-5d8a-4659-ab57-3c235face8cf">GetServiceObjectId</a>
</td>
<td align="left" width="63%">
Retrieves an object identifier for the service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/345102d4-3dac-4878-9196-bb0d97c0df07">Methods</a>
</td>
<td align="left" width="63%">
Retrieves methods that can be called on the service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/540d4320-42d4-48f0-8445-c74ff0dc1e1a">Open</a>
</td>
<td align="left" width="63%">
Opens a connection to the service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c6c42347-145c-4be7-bea6-34b13c211cb1">SendCommand</a>
</td>
<td align="left" width="63%">
Sends a command and its parameters to the service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4982efa9-82f2-457b-acf4-c6f7d48cf6f7">Unadvise</a>
</td>
<td align="left" width="63%">
Unregisters a service callback method.

</td>
</tr>
</table> 


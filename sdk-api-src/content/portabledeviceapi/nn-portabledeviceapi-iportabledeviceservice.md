---
UID: NN:portabledeviceapi.IPortableDeviceService
title: IPortableDeviceService (portabledeviceapi.h)
description: Provides access to a service.
helpviewer_keywords: ["IPortableDeviceService","IPortableDeviceService interface [Windows Portable Devices SDK]","IPortableDeviceService interface [Windows Portable Devices SDK]","described","portabledeviceapi/IPortableDeviceService","wpdsdk.iportabledeviceservice"]
old-location: wpdsdk\iportabledeviceservice.htm
tech.root: wpdsdk
ms.assetid: f57344d5-c978-4c27-b8a9-b42492bd9312
ms.date: 12/05/2018
ms.keywords: IPortableDeviceService, IPortableDeviceService interface [Windows Portable Devices SDK], IPortableDeviceService interface [Windows Portable Devices SDK],described, portabledeviceapi/IPortableDeviceService, wpdsdk.iportabledeviceservice
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPortableDeviceService
 - portabledeviceapi/IPortableDeviceService
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceAPI.h
api_name:
 - IPortableDeviceService
---

# IPortableDeviceService interface


## -description

The <b>IPortableDeviceService</b> interface provides access to a service.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPortableDeviceService</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPortableDeviceService</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceservice-advise">Advise</a>
</td>
<td align="left" width="63%">
Registers an application-defined callback object that receives service events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceservice-cancel">Cancel</a>
</td>
<td align="left" width="63%">
Cancels a pending service operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceservice-capabilities">Capabilities</a>
</td>
<td align="left" width="63%">
Retrieves the service capabilities.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceservice-close">Close</a>
</td>
<td align="left" width="63%">
Releases the connection to the service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceservice-content">Content</a>
</td>
<td align="left" width="63%">
Retrieves access to the service content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceservice-getpnpserviceid">GetPnPServiceId</a>
</td>
<td align="left" width="63%">
Retrieves a Plug and Play (PnP) identifier for the service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceservice-getserviceobjectid">GetServiceObjectId</a>
</td>
<td align="left" width="63%">
Retrieves an object identifier for the service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceservice-methods">Methods</a>
</td>
<td align="left" width="63%">
Retrieves methods that can be called on the service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceservice-open">Open</a>
</td>
<td align="left" width="63%">
Opens a connection to the service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceservice-sendcommand">SendCommand</a>
</td>
<td align="left" width="63%">
Sends a command and its parameters to the service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceservice-unadvise">Unadvise</a>
</td>
<td align="left" width="63%">
Unregisters a service callback method.

</td>
</tr>
</table>


---
UID: NN:portabledeviceapi.IPortableDeviceServiceManager
title: IPortableDeviceServiceManager (portabledeviceapi.h)
description: Retrieves the device associated with a service and the list of services found on a device.
helpviewer_keywords: ["IPortableDeviceServiceManager","IPortableDeviceServiceManager interface [Windows Portable Devices SDK]","IPortableDeviceServiceManager interface [Windows Portable Devices SDK]","described","portabledeviceapi/IPortableDeviceServiceManager","wpdsdk.iportabledeviceservicemanager"]
old-location: wpdsdk\iportabledeviceservicemanager.htm
tech.root: wpdsdk
ms.assetid: 8df23343-26f0-4fb0-90b9-e8b75bcadffa
ms.date: 12/05/2018
ms.keywords: IPortableDeviceServiceManager, IPortableDeviceServiceManager interface [Windows Portable Devices SDK], IPortableDeviceServiceManager interface [Windows Portable Devices SDK],described, portabledeviceapi/IPortableDeviceServiceManager, wpdsdk.iportabledeviceservicemanager
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
 - IPortableDeviceServiceManager
 - portabledeviceapi/IPortableDeviceServiceManager
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
 - IPortableDeviceServiceManager
---

# IPortableDeviceServiceManager interface


## -description

The <b>IPortableDeviceServiceManager</b> interface retrieves the device associated with a service and the list of services found on a device.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPortableDeviceServiceManager</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPortableDeviceServiceManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPortableDeviceServiceManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceforservice">GetDeviceForService</a>
</td>
<td align="left" width="63%">
Retrieves the device associated with the specified service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices">GetDeviceServices</a>
</td>
<td align="left" width="63%">
Retrieves a list of the services associated with the specified device.

</td>
</tr>
</table>
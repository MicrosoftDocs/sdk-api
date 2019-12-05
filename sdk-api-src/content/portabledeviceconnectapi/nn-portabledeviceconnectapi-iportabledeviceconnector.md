---
UID: NN:portabledeviceconnectapi.IPortableDeviceConnector
title: IPortableDeviceConnector (portabledeviceconnectapi.h)
description: Defines methods used for connection-management and property-retrieval for a paired MTP/Bluetooth device.
old-location: wpdsdk\iportabledeviceconnector.htm
tech.root: wpd_sdk
ms.assetid: c6eb1103-2395-431d-9130-1e1f2cc9ae96
ms.date: 12/05/2018
ms.keywords: IPortableDeviceConnector, IPortableDeviceConnector interface [Windows Portable Devices SDK], IPortableDeviceConnector interface [Windows Portable Devices SDK],described, portabledeviceconnectapi/IPortableDeviceConnector, wpdsdk.iportabledeviceconnector
ms.topic: interface
f1_keywords:
- portabledeviceconnectapi/IPortableDeviceConnector
dev_langs:
- c++
req.header: portabledeviceconnectapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Portabledeviceconnectapi.idl
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
- portabledeviceconnectapi.h
api_name:
- IPortableDeviceConnector
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPortableDeviceConnector interface


## -description


The <b>IPortableDeviceConnector</b> interface defines methods used for connection-management and property-retrieval for a paired MTP/Bluetooth device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPortableDeviceConnector</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPortableDeviceConnector</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPortableDeviceConnector</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-cancel">Cancel</a>
</td>
<td align="left" width="63%">
Cancels a pending request to connect or disconnect an MTP Bluetooth device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect">Connect</a>
</td>
<td align="left" width="63%">
Sends an asynchronous connection request to the MTP Bluetooth device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect">Disconnect</a>
</td>
<td align="left" width="63%">
Sends an asynchronous disconnect request to the MTP Bluetooth device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-getpnpid">GetPnPID</a>
</td>
<td align="left" width="63%">
Retrieves the connector's Plug and Play (PnP) device identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-getproperty">GetProperty</a>
</td>
<td align="left" width="63%">
Retrieves a bus-level property for the given MTP Bluetooth device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-setproperty">SetProperty</a>
</td>
<td align="left" width="63%">
Sets a property for the given MTP Bluetooth Bus Enumerator device.

</td>
</tr>
</table> 


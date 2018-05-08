---
UID: NN:portabledeviceconnectapi.IEnumPortableDeviceConnectors
title: IEnumPortableDeviceConnectors
author: windows-driver-content
description: Supports the enumeration of IPortableDeviceConnector interfaces, representing MTP/Bluetooth devices that were paired with the PC.
old-location: wpdsdk\ienumportabledeviceconnectors.htm
old-project: wpd_sdk
ms.assetid: 99aa1e89-5e20-4f6e-82b5-acf63305eba0
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: IEnumPortableDeviceConnectors, IEnumPortableDeviceConnectors interface [Windows Portable Devices SDK], IEnumPortableDeviceConnectors interface [Windows Portable Devices SDK],described, devpkey/IEnumPortableDeviceConnectors, portabledeviceconnectapi/IEnumPortableDeviceConnectors, wpdsdk.ienumportabledeviceconnectors
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: PNRPINFO_V2, *PPNRPINFO_V2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	PortableDeviceGuids.lib
-	PortableDeviceGuids.dll
api_name:
-	IEnumPortableDeviceConnectors
product: Windows
targetos: Windows
req.lib: PortableDeviceGuids.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IEnumPortableDeviceConnectors interface


## -description


The <b>IEnumPortableDeviceConnectors</b> interface supports the enumeration of <a href="https://msdn.microsoft.com/c6eb1103-2395-431d-9130-1e1f2cc9ae96">IPortableDeviceConnector</a> interfaces, representing MTP/Bluetooth devices that were paired with the PC.  Note that this will retrieve all previously-paired devices, including devices that are paired but disconnected. To determine if a device is still connected, query the <b>DEVPKEY_MTPBTH_IsConnected</b> property for that device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumPortableDeviceConnectors</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumPortableDeviceConnectors</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumPortableDeviceConnectors</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938510">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the current <b>IEnumPortableDeviceConnectors</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926903">Next</a>
</td>
<td align="left" width="63%">
Retrieves the next one or more <a href="https://msdn.microsoft.com/c6eb1103-2395-431d-9130-1e1f2cc9ae96">IPortableDeviceConnector</a> objects in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926952">Skip</a>
</td>
<td align="left" width="63%">
Skips the specified number of devices in the enumeration sequence.

</td>
</tr>
</table> 


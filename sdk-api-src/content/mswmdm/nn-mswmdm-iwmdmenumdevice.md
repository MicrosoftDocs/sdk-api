---
UID: NN:mswmdm.IWMDMEnumDevice
title: IWMDMEnumDevice (mswmdm.h)
author: windows-sdk-content
description: The IWMDMEnumDevice interface enumerates portable devices attached to a computer. To obtain this interface, call IWMDeviceManager::EnumDevices.
old-location: wmdm\iwmdmenumdevice.htm
tech.root: WMDM
ms.assetid: fcb93d2a-2107-4aa9-9b3a-130044d7dc96
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMDMEnumDevice, IWMDMEnumDevice interface [windows Media Device Manager], IWMDMEnumDevice interface [windows Media Device Manager],described, IWMDMEnumDeviceInterface, mswmdm/IWMDMEnumDevice, wmdm.iwmdmenumdevice
ms.topic: interface
req.header: mswmdm.h
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
 - mswmdm.h
api_name:
 - IWMDMEnumDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMDMEnumDevice interface


## -description



The <b>IWMDMEnumDevice</b> interface enumerates portable devices attached to a computer. To obtain this interface, call <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices">IWMDeviceManager::EnumDevices</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDMEnumDevice</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMDMEnumDevice</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDMEnumDevice</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumdevice-clone">Clone</a>
</td>
<td align="left" width="63%">
Returns a copy of the <b>IWMDMEnumDevice</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumdevice-next">Next</a>
</td>
<td align="left" width="63%">
Returns a pointer to the next device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumdevice-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration so that <b>Next</b> returns a pointer to the first device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumdevice-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips over a specified number of devices in the enumeration sequence.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMDM/enumerating-devices">Enumerating Devices</a>



<a href="https://docs.microsoft.com/windows/desktop/WMDM/interfaces-for-applications">Interfaces for Applications</a>
 

 


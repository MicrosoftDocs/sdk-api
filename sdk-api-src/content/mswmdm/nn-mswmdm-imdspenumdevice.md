---
UID: NN:mswmdm.IMDSPEnumDevice
title: IMDSPEnumDevice (mswmdm.h)
author: windows-sdk-content
description: The IMDSPEnumDevice interface is used to enumerate the media devices.
old-location: wmdm\imdspenumdevice.htm
tech.root: WMDM
ms.assetid: 9a296937-6f8b-4f04-989f-3a5d4c6f7b85
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMDSPEnumDevice, IMDSPEnumDevice interface [windows Media Device Manager], IMDSPEnumDevice interface [windows Media Device Manager],described, IMDSPEnumDeviceInterface, mswmdm/IMDSPEnumDevice, wmdm.imdspenumdevice
ms.topic: interface
f1_keywords: 
 - "mswmdm/IMDSPEnumDevice"
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
 - IMDSPEnumDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMDSPEnumDevice interface


## -description



The <b>IMDSPEnumDevice</b> interface is used to enumerate the media devices. For more information on enumeration, see the Microsoft COM documentation on the COM page at the <a href="http://go.microsoft.com/fwlink/p/?linkid=3282">Microsoft Web site</a>. The <b>IMDSPEnumDevice</b> interface is implemented on the device enumerator object. The only valid way to create a device enumerator object is to call <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider-enumdevices">IMDServiceProvider::EnumDevices</a>. If the device implements <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice">IMDServiceProvider2::CreateDevice</a>, this enumerator should enumerate only non-Plug and Play devices. The device enumerator should enumerate only the devices that are attached to the computer and are supported by the service provider.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMDSPEnumDevice</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMDSPEnumDevice</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMDSPEnumDevice</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspenumdevice-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates another enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspenumdevice-next">Next</a>
</td>
<td align="left" width="63%">
Returns a pointer to the next <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice">IMDSPDevice</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspenumdevice-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspenumdevice-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips over the next specified number of media device interface(s) in the enumeration sequence.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice">IMDSPDevice Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider-enumdevices">IMDServiceProvider::EnumDevices</a>



<a href="https://docs.microsoft.com/windows/desktop/WMDM/interfaces-for-service-providers">Interfaces for Service Providers</a>
 

 


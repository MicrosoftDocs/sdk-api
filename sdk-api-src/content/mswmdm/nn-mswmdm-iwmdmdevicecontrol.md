---
UID: NN:mswmdm.IWMDMDeviceControl
title: IWMDMDeviceControl (mswmdm.h)
author: windows-sdk-content
description: The IWMDMDeviceControl interface provides methods for controlling playback on a device.
old-location: wmdm\iwmdmdevicecontrol.htm
tech.root: WMDM
ms.assetid: e7b58957-4795-461f-ae3d-fb80e6711c9f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMDMDeviceControl, IWMDMDeviceControl interface [windows Media Device Manager], IWMDMDeviceControl interface [windows Media Device Manager],described, IWMDMDeviceControlInterface, mswmdm/IWMDMDeviceControl, wmdm.iwmdmdevicecontrol
ms.topic: interface
f1_keywords: 
 - "mswmdm/IWMDMDeviceControl"
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
 - IWMDMDeviceControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMDMDeviceControl interface


## -description



The <b>IWMDMDeviceControl</b> interface provides methods for controlling playback on a device. Query an <b>IWMDMDevice</b> interface to get this interface. Playback parameters are controlled by the <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmobjectinfo">IWMDMObjectInfo</a> interface.

The <b>IWMDMDeviceControl</b> interface methods support several modes of audio control, depending on the context in which they are used. That context is defined by the <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevicecontrol-seek">IWMDMDeviceControl::Seek</a> method. The <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevicecontrol-getcapabilities">IWMDMDeviceControl::GetCapabilities</a> method is used to determine what kinds of operations can be performed by the device.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDMDeviceControl</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMDMDeviceControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDMDeviceControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevicecontrol-getcapabilities">GetCapabilities</a>
</td>
<td align="left" width="63%">
Retrieves the device capabilities to determine what operations the device can perform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevicecontrol-getstatus">GetStatus</a>
</td>
<td align="left" width="63%">
Retrieves the control status of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevicecontrol-pause">Pause</a>
</td>
<td align="left" width="63%">
Pauses the current play or record operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevicecontrol-play">Play</a>
</td>
<td align="left" width="63%">
Begins playing at the current seek position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevicecontrol-record">Record</a>
</td>
<td align="left" width="63%">
Begins recording from the device's external record input at the current seek position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevicecontrol-resume">Resume</a>
</td>
<td align="left" width="63%">
Resumes the current play or record operation from the file position saved during the call to <b>Pause</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevicecontrol-seek">Seek</a>
</td>
<td align="left" width="63%">
Seeks to a position that is used as the starting point by the <b>Play</b> or <b>Record</b> methods.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevicecontrol-stop">Stop</a>
</td>
<td align="left" width="63%">
Stops the current record or play operation.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMDM/interfaces-for-applications">Interfaces for Applications</a>
 

 


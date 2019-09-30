---
UID: NN:mswmdm.IMDSPDeviceControl
title: IMDSPDeviceControl (mswmdm.h)
author: windows-sdk-content
description: The IMDSPDeviceControl interface provides methods for controlling devices.
old-location: wmdm\imdspdevicecontrol.htm
tech.root: WMDM
ms.assetid: a196edef-f670-4c1f-92bd-172a75f3f420
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMDSPDeviceControl, IMDSPDeviceControl interface [windows Media Device Manager], IMDSPDeviceControl interface [windows Media Device Manager],described, IMDSPDeviceControlInterface, mswmdm/IMDSPDeviceControl, wmdm.imdspdevicecontrol
ms.topic: interface
f1_keywords: 
 - "mswmdm/IMDSPDeviceControl"
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
 - IMDSPDeviceControl
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMDSPDeviceControl interface


## -description



The <b>IMDSPDeviceControl</b> interface provides methods for controlling devices. After this interface is acquired from a specific instance of the <b>IMDSPDevice</b> interface, the control methods are used for remote control of streaming audio play, record, pause, stop, and seek operations on that device. Implementing this interface is optional. For more information, see <a href="https://docs.microsoft.com/windows/desktop/WMDM/mandatory-and-optional-interfaces">Mandatory and Optional Interfaces</a>.

The <b>IMDSPDeviceControl</b> interface methods support several modes of audio control, depending on the context in which they are used. That context is defined by the <b>Seek</b> method. The <b>GetCapabilities</b> method is used to determine what kinds of operations can be performed by the device.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMDSPDeviceControl</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMDSPDeviceControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMDSPDeviceControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevicecontrol-getcapabilities">GetCapabilities</a>
</td>
<td align="left" width="63%">
Retrieves the device capabilities to determine what operations the device can perform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevicecontrol-getdcstatus">GetDCStatus</a>
</td>
<td align="left" width="63%">
Retrieves the control status of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevicecontrol-pause">Pause</a>
</td>
<td align="left" width="63%">
Pauses the current playback or record operation and saves the current file position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevicecontrol-play">Play</a>
</td>
<td align="left" width="63%">
Begins playing at the current seek position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevicecontrol-record">Record</a>
</td>
<td align="left" width="63%">
Begins recording from the device's external record input at the current seek position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevicecontrol-resume">Resume</a>
</td>
<td align="left" width="63%">
Resumes the current playback or record operation from the file position saved during the call to <b>Pause</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevicecontrol-seek">Seek</a>
</td>
<td align="left" width="63%">
Seeks to a position that is used as the starting point by the <b>Play</b> or <b>Record</b> methods.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevicecontrol-stop">Stop</a>
</td>
<td align="left" width="63%">
Stops the current playback or record operation.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMDM/interfaces-for-service-providers">Interfaces for Service Providers</a>
 

 


---
UID: NN:mswmdm.IWMDMDeviceControl
title: IWMDMDeviceControl
author: windows-sdk-content
description: The IWMDMDeviceControl interface provides methods for controlling playback on a device.
old-location: wmdm\iwmdmdevicecontrol.htm
old-project: WMDM
ms.assetid: e7b58957-4795-461f-ae3d-fb80e6711c9f
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWMDMDeviceControl, IWMDMDeviceControl interface [windows Media Device Manager], IWMDMDeviceControl interface [windows Media Device Manager],described, IWMDMDeviceControlInterface, mswmdm/IWMDMDeviceControl, wmdm.iwmdmdevicecontrol
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mswmdm.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: MSVidCtlStateList
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
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IWMDMDeviceControl interface


## -description



The <b>IWMDMDeviceControl</b> interface provides methods for controlling playback on a device. Query an <b>IWMDMDevice</b> interface to get this interface. Playback parameters are controlled by the <a href="https://msdn.microsoft.com/ebc6ad10-02c1-4cc9-8a09-d1fe7aef146a">IWMDMObjectInfo</a> interface.

The <b>IWMDMDeviceControl</b> interface methods support several modes of audio control, depending on the context in which they are used. That context is defined by the <a href="https://msdn.microsoft.com/f416a520-197c-4607-979e-8f43951f2076">IWMDMDeviceControl::Seek</a> method. The <a href="https://msdn.microsoft.com/61d0e44c-f1be-4837-a773-48c6c5278fe0">IWMDMDeviceControl::GetCapabilities</a> method is used to determine what kinds of operations can be performed by the device.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDMDeviceControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMDMDeviceControl</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/61d0e44c-f1be-4837-a773-48c6c5278fe0">GetCapabilities</a>
</td>
<td align="left" width="63%">
Retrieves the device capabilities to determine what operations the device can perform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e39fb2ed-a3b4-4167-9404-6b7c706f0941">GetStatus</a>
</td>
<td align="left" width="63%">
Retrieves the control status of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/420963d1-11ea-4f1d-b5c0-749e99ee7725">Pause</a>
</td>
<td align="left" width="63%">
Pauses the current play or record operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e8d717e6-365c-44ad-b24e-daa3c35664de">Play</a>
</td>
<td align="left" width="63%">
Begins playing at the current seek position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a9372ce9-e339-4664-9e12-4feae29529dc">Record</a>
</td>
<td align="left" width="63%">
Begins recording from the device's external record input at the current seek position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/24ee343c-09ed-4a5f-b7be-eba15dcc4b36">Resume</a>
</td>
<td align="left" width="63%">
Resumes the current play or record operation from the file position saved during the call to <b>Pause</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f416a520-197c-4607-979e-8f43951f2076">Seek</a>
</td>
<td align="left" width="63%">
Seeks to a position that is used as the starting point by the <b>Play</b> or <b>Record</b> methods.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/842b7de7-dde2-40d1-8028-9ffebcaea90e">Stop</a>
</td>
<td align="left" width="63%">
Stops the current record or play operation.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/bea867d6-a875-4150-9958-7f683cd215b9">Interfaces for Applications</a>
 

 


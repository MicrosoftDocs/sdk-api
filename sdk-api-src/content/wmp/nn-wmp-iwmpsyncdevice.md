---
UID: NN:wmp.IWMPSyncDevice
title: IWMPSyncDevice (wmp.h)
author: windows-sdk-content
description: The IWMPSyncDevice interface represents a device to which Windows Media Player 10 or later can copy digital media files.
old-location: wmp\iwmpsyncdevice.htm
tech.root: WMP
ms.assetid: 981648e4-0cb1-4d7a-bd3b-50e1b9a7282c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMPSyncDevice, IWMPSyncDevice interface [Windows Media Player], IWMPSyncDevice interface [Windows Media Player],described, IWMPSyncDeviceInterface, wmp.iwmpsyncdevice, wmp/IWMPSyncDevice
ms.topic: interface
f1_keywords: 
 - "wmp/IWMPSyncDevice"
req.header: wmp.h
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
 - wmp.h
api_name:
 - IWMPSyncDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPSyncDevice interface


## -description



The <b>IWMPSyncDevice</b> interface represents a device to which Windows Media Player 10 or later can copy digital media files. It provides methods used to specify and retrieve properties for the device and to manage the relationship between Windows Media Player and the device.

To use this interface, you must create a remoted instance of the Windows Media Player 10 or later control.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPSyncDevice</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMPSyncDevice</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPSyncDevice</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-createpartnership">createPartnership</a>
</td>
<td align="left" width="63%">
Creates a partnership between Windows Media Player and the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-deletepartnership">deletePartnership</a>
</td>
<td align="left" width="63%">
Terminates the partnership between Windows Media Player and the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_connected">get_connected</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the device is connected to Windows Media Player.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_deviceid">get_deviceId</a>
</td>
<td align="left" width="63%">
Retrieves the device identifier string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_devicename">get_deviceName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_friendlyname">get_friendlyName</a>
</td>
<td align="left" width="63%">
Retrieves the user-defined name of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_partnershipindex">get_partnershipIndex</a>
</td>
<td align="left" width="63%">
Retrieves the index of the device partnership.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_progress">get_progress</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating the synchronization progress as percent complete.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status">get_status</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating the status of the relationship between Windows Media Player and the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_syncstate">get_syncState</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating the current synchronization state for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-getiteminfo">getItemInfo</a>
</td>
<td align="left" width="63%">
Retrieves a metadata value from the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-isidentical">isIdentical</a>
</td>
<td align="left" width="63%">
Compares the device to the specified device and retrieves a value indicating whether they are the same device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-put_friendlyname">put_friendlyName</a>
</td>
<td align="left" width="63%">
Specifies the user defined name of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-showsettings">showSettings</a>
</td>
<td align="left" width="63%">
Displays the Windows Media Player synchronization settings dialog box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-start">start</a>
</td>
<td align="left" width="63%">
Begins synchronization.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-stop">stop</a>
</td>
<td align="left" width="63%">
Ends synchronization.

</td>
</tr>
</table> 

Retrieve a pointer to <b>IWMPSyncDevice</b> by calling  <a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsyncservices-getdevice">IWMPSyncServices::getDevice</a>.

	


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMP/interfaces">Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/WMP/remoting-the-windows-media-player-control">Remoting the Windows Media Player Control</a>
 

 

